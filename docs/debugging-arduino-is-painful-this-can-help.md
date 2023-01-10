# 调试 Arduino 是痛苦的:这有所帮助

> 原文：<https://hackaday.com/2018/11/07/debugging-arduino-is-painful-this-can-help/>

如果您习惯于使用除 Arduino IDE 之外的几乎任何现代工具进行编码，那么您可能已经习惯了片上调试。有时候，在代码中拥有这种可见性对于消除 bug 来说至关重要。但是对于 Arduino，我们大多数人只是在代码中打印语句来观察行为。当代码运行时，我们取出打印语句。[joalopesf]想要更好的东西。所以他创建了一个 Arduino 库和一个桌面应用程序，让你有一个更好的窗口来观察你的程序的执行。

老实说，它并不是您通常认为的调试器。但是它确实提供了几个不错的特性。最基本的是提供消息传递的级别，这样你就可以过滤掉你不关心的消息。这有点像服务器的日志严重性系统。有些消息是警告，有些是信息性的，有些是详细的。您可以选择要查看的邮件。

此外，库会给消息加上时间戳，这样您就可以知道消息之间经过了多长时间，以及在消息期间您使用了什么功能。它还可以检查和设置您预先配置的全局变量，并设置对变量的监视。也可以从串行监视器调用函数。

有一个[配套的 Java 程序](https://github.com/JoaoLopesF/SerialDebug/tree/master/SerialDebugApp)(见下面的视频)虽然你可以直接使用普通串行监视器的大多数功能，但它并不漂亮。如果您愿意，Java 程序也可以读取 Arduino 程序文件，并转换其中的所有打印调用以使用该库。

如你所料，这需要你的程序的一些配合。您必须设置库和串行端口。还必须安排 main 函数频繁运行(比如在主循环中)。默认情况下，调试大多被禁止(尽管您可以更改这一点)。您必须发出一个串行端口命令来打开更高级别的日志记录和调试功能。

如果您从库附带的示例开始(对基于 AVR 的 Arduino 使用简单的示例，对任何其他的 Arduino 使用高级的示例)，您会看到一些#定义，您可以使用它们来控制库:

*   DEBUG _ DISABLED–设置为 true，库编译出来没有开销
*   DEBUG _ DISABLE _ DEBUGGER–关闭除消息记录之外的所有功能
*   DEBUG _ INITIAL _ LEVEL–调试消息的起始级别
*   DEBUG _ USE _ FLASH _ F–将调试消息存储在闪存中

代码实际上有两个版本:一个用于 8 位 AVR 处理器，另一个用于其他 Arduino 类型。我们发现构建这两者都有问题。文件 src/utility/Fields.cpp、src/utility/Vector.h 和
src/utility/Util.cpp 引用 arduino.h，该文件在具有不区分大小写的文件系统的计算机上工作。在每种情况下，对于 Linux，它需要是 Arduino.h。此外，SerialDebug.cpp 缺少 stdarg.h include。我们已经向开发人员报告了这两个问题，所以现在可能已经解决了。

您可以浏览视频和文档来了解它是如何工作的。它是一个成熟的调试器吗？不可以。你不能停止执行(奇怪，因为技术上你肯定可以)，设置断点，或者单步执行。但是至少能够访问程序的一些内部状态仍然是有用的。

当然，Arduino 已经[承诺很快](https://hackaday.com/2018/05/18/arduino-just-introduced-an-fpga-board-announces-debugging-and-better-software/#more-308281)全面调试。我们甚至看到一个 [Arduino 通过 debugWIRE 调试另一个](https://hackaday.com/2018/02/07/debugging-an-arduino-with-an-arduino/)。

 [https://www.youtube.com/embed/C4qRwwjyZwg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/C4qRwwjyZwg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

