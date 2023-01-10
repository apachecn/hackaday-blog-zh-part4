# Beyond Printf():更好的日志实践，用于更快的调试

> 原文：<https://hackaday.com/2020/07/21/beyond-printf-better-logging-practices-for-faster-debugging/>

我们所有从事编程的人都知道，日志记录是一种经过时间考验的方法，可以输出关于代码内部状态的消息。这些消息具有不同程度的可调粒度，使我们不仅可以跟踪应用程序的状态，还可以跟踪它的整体健康状况。当事情最终变得更糟时，这些日志信息通常是我们首先要考虑的，它相当于飞机上的飞行数据记录器。

花一些时间和精力不仅设计日志系统，而且决定什么应该被记录，在什么级别，可以让我们未来的自己更加欣赏生活。我们都熟悉“printf-debugging”的做法，在这种情况下，日志记录被添加为通常的崩溃后尸检的一部分，因为人们试图找出到底哪里出了问题。这是一种方法，而且最终会奏效，但是我们可以做得更好。

人们是懒惰的，只有当良好的日志记录实践至少和在代码中散布 printf()语句一样简单时，您才会坚持这样的实践。然而，与此同时，我们希望能够处理像日志级别和换行符这样的事情，而不需要太多的额外输入。最成功的日志库就是用这个构建的

## 设置背景

并非每个应用程序都需要相同类型的日志记录。在决定适合您需求的日志记录时，请考虑项目的背景。

许多嵌入式平台是高度特定于应用的。无论是洗衣机内的简单 8 位 MCU 还是强大的基于 SoC 的系统，微波炉的 MCU 固件都不需要与汽车 ECU 或工业 PID 控制器相同的日志记录水平。然而，它们都受益于良好的日志记录实践，无论这些消息是被存储，还是仅在主动调试硬件时可见。

对于服务器应用程序来说，日志记录是操作中非常重要的一部分，因为系统管理员希望从一个中心位置读取在他们负责的服务器上运行的所有服务的日志。这意味着这些日志应该只包含系统管理员可能会觉得有用的信息，而不是开发人员会寻找的信息。

桌面平台是相似的，在大多数平台上，中央日志服务将记录任何正在运行的服务的标准输出。对于常规应用程序(即非服务)，任何日志记录输出往往要么是更短暂的东西。标准输出要么显示在终端窗口中，要么消失在空白中，没有与之关联的终端或其他输出。出于本文的考虑，我们将假设我们只需写入 stdout，而无需考虑任何进一步的细节。

作为一个小题外话，[移动平台](https://en.wikipedia.org/wiki/Mobile_operating_system)对于日志来说是一个相当特殊的例子。在记录每个应用程序的标准输出的意义上，它们更类似于服务器平台。通过这种方式，用户可以获得正在运行的每个服务和应用程序的日志，而无需进行任何配置。如何在 Android、iOS、Tizen 或 ChromeOS 等移动平台上获取该日志的具体细节因平台而异。

## 明智地使用日志级别

您可能会问，为什么要有日志级别？因为您希望区分日志消息的重要性，甚至可能只过滤特定类型的消息。常见的日志级别有:

1.  致命的。
2.  危急关头。
3.  错误。
4.  警告。
5.  注意。
6.  信息。
7.  调试。
8.  追踪。

通常情况下，您会在最多为“信息”级别的日志级别运行服务，但是如果服务在此日志级别过于“喋喋不休”,您可能会希望将其删除以引起注意，甚至只是发出警告。因此，开发人员有责任正确考虑他们将要添加到代码中的消息应该存在于哪个日志级别。这是一条信息性消息吗？至少应该看一遍的通知？或者这是一个必须解决的警告？

显然，错误级别的消息是坏消息，但是我们还有两个级别。这里的“严重”级别应该用于介于“嗯，混蛋”和“系统着火了”之间的错误。接下来,“致命”消息包括服务达到不可恢复的状态、致命的运行时错误，以及任何可能意味着系统管理员将在周六凌晨 3 点被从床上叫起来的事情。

最后，“调试”级别是指在调试代码时有用的信息，比如某些变量的值和应用程序活动的详细日志。对于真正细粒度的调试输出，有一个“跟踪”级别，它是针对冗长的信息。这通常用于最大详细记录。

## 使用 Poco::Logger；—一个基于服务器的实用示例

多年来，我不得不将日志添加到业余爱好和商业项目中。我最喜欢的是一个嵌入式服务器项目，它可以在世界各地无数无头系统上运行，唯一的反馈是内置的日志记录，可以通过正确的软件读取并发送回总部。为此，我使用了来自 [libPoco](https://pocoproject.org/) 库的 [Poco::Logger](https://pocoproject.org/docs/Poco.Logger.html) 。它负责更繁琐的事情，比如将不同的日志流(通道)聚集在一起以及其他后勤工作。

正确的日志记录不仅对我自己诊断问题至关重要，对同事来说也是如此，他们可以使用相同的日志记录，通过跟踪请求及其数据来找出哪里(以及为什么)开始着火了。它工作得很好，而且我已经在我的一些爱好项目中使用了同样的日志记录，包括 C++中的远程过程调用(RPC)库 [NymphRPC](https://github.com/MayaPosch/NymphRPC) 。我实现的部分包含在 [nymph_logger.h](https://github.com/MayaPosch/NymphRPC/blob/master/src/nymph_logger.h) 和 [nymph_logger.cpp](https://github.com/MayaPosch/NymphRPC/blob/master/src/nymph_logger.cpp) 中。它允许基于 NymphRPC 的应用程序写入日志，如下所示:

```

NYMPH_LOG_DEBUG("Added new connection with handle: " + NumberFormatter::format(handle));

```

`NYMPH_LOG_DEBUG ()`部分是一个预处理宏，在 nymph_logger.h 中定义为:

```

#define NYMPH_LOG_DEBUG(msg) \
	if (NymphLogger::priority >= Poco::Message::PRIO_DEBUG) { \
		NymphLogger::logger(loggerName).debug(msg, __FILE__, __LINE__);\
	}

```

在这里，我们可以看到这一行是如何被 if 语句替换的，该语句检查应用程序应该在哪个日志级别进行日志记录。预处理语句使我们不必每次都键入所有这些内容，同时还将`__FILE__`和`__LINE__`文本扩展到当前文件名和使用 log 语句的(未处理的)源代码行中。静态的`NymphLogger::logger()`调用返回一个特定的日志记录器，它是`Poco::Logger`的一个实例。

单个`NymphLoggerChannel`(继承自`Poco::Channel`)被提供给`Poco::Logger`作为输出通道。这个通道只是将一个格式化的字符串和日志级别一起传递给一个外部提供的函数指针，从这里可以将它打印到 stdout，写入文件，存储在数据库中，或者其他任何合适的东西。

格式化代码:

```

	string msgStr;
	msgStr = NumberFormatter::format(msg.getPid());
	msgStr += "." + NumberFormatter::format(msg.getTid());
	msgStr += "\t" + msg.getSource() + "\t";
	msgStr += NumberFormatter::format(msg.getSourceLine()) + "\t";
	msgStr += msg.getText() + "\t\t- ";
	msgStr += msg.getSourceFile();

	(*loggerFunction)(level, msgStr);

```

当我们运行 NymphRPC 测试客户端和服务器时，我们可以看到如下所示的日志输出:

```

6 - 14524.2     NymphSession    130     Read 37 bytes.          - src/nymph_session.cpp
6 - 14524.2     NymphMessage    79      Method ID: 2\.           - src/nymph_message.cpp
6 - 14524.2     NymphMessage    93      Message flags: 0x0              - src/nymph_message.cpp
6 - 14524.2     NymphUtilities  170     NYMPH_TYPE_STRING               - src/nymph_utilities.cpp
6 - 14524.2     NymphTypes      306     String value: callbackFunction.         - src/nymph_types.cpp
6 - 14524.2     NymphSession    148     Calling method callback for message ID: 0x3             - src/nymph_session.cpp
6 - 14524.2     NymphMethod     92      Calling callback for method: helloCallbackFunction              - src/nymph_method.cpp

```

查看测试服务器的代码，我们可以看到第一个数字是日志级别(6: Debug)，其余的是之前格式化的字符串。它包含进程 ID、该进程中记录消息的线程、记录器的名称、源代码中的行、消息，最后是源文件的相对路径(来自 Makefile)。

## 最后的想法

我发现，不得不经常吃自己的狗粮，还要处理同事和客户对自己代码的日志输出的评论，这极大地激励了我去打磨粗糙的地方。本文无法涵盖的一个问题是在代码中记录什么是重要的。这是您，开发人员，已经知道的事情，或者将通过挖掘日志文件时的痛苦经历发现的事情。

也就是说，爱好项目是尝试不同日志方法的好地方。一旦你发现自己在做一个商业项目，想有创意肯定是来不及了。从积极的一面来看，一旦你知道如何在不同的情况下正确地进行日志记录，它可以将周末的 bug 搜索会议变成周五下午的一个简短的 10 分钟日志阅读代码调整和 CI 干扰会议。