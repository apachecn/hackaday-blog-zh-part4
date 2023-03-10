# 新手机的忧郁:提醒黑客们不要妥协

> 原文：<https://hackaday.com/2022/03/22/the-new-phone-blues-a-reminder-that-hackers-shouldnt-settle/>

尽管将人类知识的总和掌握在你的手掌中很方便，也是必不可少的，但购买和配置智能手机的实际过程可能是一种令人难以置信的沮丧体验。站在手机店那些没完没了的队伍中，跳过行政管理的关卡，盯着一个将要在厕所里结束生命的设备的标签震惊，这些都导致了挫败感。

但在我看来，真正的麻烦开始了，一旦你克服了所有这些东西，开始试着把新手机安装好。当然，大多数手机制造商很容易将你的旧手机克隆到新手机上，但总是会有一些小问题。对于像手机一样紧密融入你日常生活工作流程的东西来说，这真的很糟糕。尤其是当你发现你闪亮的新手机不能做你绝对依赖的事情的时候。

## 问题是

一个很好的例子就是我本周的经历，当时我终于承认我需要一个“真正的”手机计划，而不是我和妻子十年来一直带着的预付费手机。我们得到了一笔看起来非常划算的交易——免费的全新 Pixel 6 手机，每月只需比我们目前支付的费用多 10 美元。所以我们在线注册，等待我们的手机发货。实际上，一点也不痛苦。

这应该是我对即将发生的事情的第一个暗示。Pixels 在从旧手机移植我们所有的应用程序方面做得非常好。用正确的铃声和屏幕设置把事情设置好，虽然繁琐但简单明了。然而，事情开始分崩离析的地方是一个特殊的、关键的应用程序——我们用来监测糖尿病女儿血糖水平的应用程序。

![](img/bd2d0439f3dcf0fbf08dc56cce916f73.png)

This is the data that I need access to on the new phone.

我以前写过很多关于糖尿病的文章，以及对于患有 1 型糖尿病的孩子的父母来说,[连续血糖监测(CGM)如何既是天赐之物又是诅咒。但这个应用程序将我们与她的 CGM 系统上传数据的云服务联系起来，对我们来说绝对是必不可少的。我们的女儿睡得像块石头；实际上没有什么能吵醒她，尤其是当她的血糖在半夜低到危险程度时，她的 CGM 发出的哔哔声。这意味着我们必须在手机上运行 CGM 应用程序，这样我们就可以收到她有麻烦的通知，并在严重和潜在致命的低血糖发生之前叫醒她，给她吃零食。](https://hackaday.com/2018/12/03/why-is-continuous-glucose-monitoring-so-hard/)

你知道吗，CGM 程序不能在新像素上工作。我们做了一些调查，发现供应商只认证了该应用程序与极少数手机兼容，其中不包括 Pixel 6。奇怪的是，我们的旧手机都不在名单上，但这两款手机都可以用。这就是为什么我不太关心像素——如果它运行在我妻子的老式 Moto G4 上，它应该运行在最新最棒的上，对吗？不对。

在 CGM 供应商和手机运营商的技术支持下，我在电话上浪费了一个下午，我坐下来和妻子一起吃晚饭，感觉被打败了。我们沮丧地考虑着我们不得不取消电话计划的可能性，这时我有了一个想法:*等一下！你应该是个黑客。所以，开始黑吧！*

## 特雷·哈克

我需要的是，当旧手机上的 CGM 应用程序发出警报时，我能在新手机上得到提醒。我意识到我的旧手机，CGM 应用程序现在运行良好，将成为我黑客的核心。我的旧手机上的另一个资产是 MacroDroid，这是一个脚本工具，我用来确保如果我女儿的闹钟在半夜响起超过五次，我会通过发出一个超级讨厌的警报来醒来——深度睡眠是家族遗传。

不幸的是，旧手机都没有 SIM 卡了，所以通过短信或彩信给新手机发短信是不可能的。我试着发了一封电子邮件，但是效果一直不好。然后我偶然发现了 [ClickSend](https://www.clicksend.com/us/) ，一种专门为营销目的发送大量短信的服务——你知道，垃圾短信。但是，他们有一个 API，让我编写一个 HTTP GET 请求，向我们的手机发送一个简短的文本。幸运的是，MacroDroid 支持 get 作为它可以执行的操作之一。

因此，经过一个上午的努力，我想出了一个暂时足够好的解决办法。如果我女儿的 CGM 感应到低血糖事件，我旧手机上的应用程序会设置一个通知，MacroDroid 会将其识别为触发器。然后，它向 ClickSend 发送 GET 请求，click send 会立即向我们的新手机发送一条消息。我所要做的就是让我的旧手机在我的桌子上开机，这几乎和让原生应用程序在 Pixel 上工作一样好。

## 下一步措施和经验教训

![](img/f816d0c744c5bae31f9201b789358d05.png)

It works! My daughter was out for the day, and the old phone (right) sent an SMS to the new phone when her blood glucose dropped below the limit.

完美吗？远非如此。我喜欢在手机上安装完整的 CGM 应用程序带来的便利，并且可以随时查看她的号码。同样重要的是要看她的图表，判断如何治疗她——稳定在 80 mg/dL 和 55 mg/dL 与快速下降之间有很大的区别。无法即时获得这些信息需要一些时间来适应。

但我对这种变通办法的最大问题是，它依赖于一长串的依赖性——我的旧手机工作，我的 WiFi 和 ISP 保持在线，CGM 供应商的云应用程序中没有服务中断，以及点击发送启动并运行。有很多东西会坏掉。我真的很想去掉所有这些中间人，建立一个小部件，直接接收来自我女儿的 CGM 的 RF 信号，如果她下降，就会发出一些本地警报。我想象一个床头柜，它可以让房间的灯闪烁，或者启动摇床，或者，你知道，T2 向她扔标枪。糖尿病肯定有某种好处。

在我有时间建造这样的东西之前，这个黑客将不得不这么做。这是一个伟大的黑客时代吗？一点也不。它是一个快速的黑客，我能够用我手头的东西来解决一个具体的硬件问题。在我看来，这就是胜利。

但我认为这里最大的教训是，有时很容易忘记你到底是谁。我让自己被这个过程打败，到了一个我看不到我有办法解决这个问题的地步。归根结底，黑客是一种乐观主义——它是关于不接受系统输出的东西，并找到另一种解决方案的方法。在这种时候，我们需要尽可能乐观。