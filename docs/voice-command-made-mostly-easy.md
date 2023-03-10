# 语音命令变得非常简单

> 原文：<https://hackaday.com/2021/12/27/voice-command-made-mostly-easy/>

从数字助理到汽车，语音命令风靡一切。将它添加到您自己的项目中需要大量的工作，对吗？也许不是。[Electronoobs]展示了一个[语音板](https://www.youtube.com/watch?v=zCEYxSdYBcA)，可以让你通过与主机的串行通信轻松集成 255 个语音命令。你可以在下面的视频中看到评论。

他以前实际上使用过类似的板，但那是几年前的版本，当然，新模块有许多新功能。从 3.1 版本开始，该板可以比旧版本更灵活地处理 255 个命令。

尽管该板可以处理 255 条命令，但它一次只能监听其中的 7 条，这是一个奇怪的限制。然而，旧的板有更严格的限制，你只能听三组中的一组，每组有 5 个命令。有了新的板，你可以选择 255 个命令中的任何 7 个命令同时激活。然后，您可以根据上下文用其他命令替换这 7 个命令中的一些。例如，您可能会监听一个主菜单命令，并根据该选择监听另一组二级命令

接口要么是串行的，要么是 I ² C。我们不禁想到，如果你能同时监听 12 或 15 个命令，你就能拥有一套监听数字的设备，这可能会很方便。也许第四版？

您可以使用带有交互式向导式设置的麦克风来训练命令。这项技术的最终目标是机器人，但目前[电子人]只是根据命令点亮发光二极管。但是只要你能算出 7 个命令的限制，它看起来很容易用于任何目的。

这很难做到，但是你可以让一个 Arduino [自己处理语音](https://www.youtube.com/watch?v=zCEYxSdYBcA)。更简单的是，用一个[更大的处理器](https://hackaday.com/2019/01/01/picovoice-puts-smarts-offline-in-512k-of-memory/)。

 [https://www.youtube.com/embed/zCEYxSdYBcA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zCEYxSdYBcA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

