# 除了输出视频做其他事情

> 原文：<https://hackaday.com/2019/01/15/do-other-things-besides-output-video/>

随着价格的下降和编程简易性的提高，小型微控制器和微型片上系统现在变得越来越受欢迎。Raspberry Pi 相对便宜，可以做你需要的几乎所有事情，但不是每个芯片都可以做我们大多数人认为理所当然的事情，如输出视频。对于许多平台来说，除了视频输出本身之外，节省任何处理器或内存用于其他任务几乎是不可能的。

[Dave]又名[Mubes]一直致力于蓝色药丸平台，这是一个 [STM32F103C8](http://wiki.stm32duino.com/index.php?title=Blue_Pill) 板。虽然它们本身并不输出视频，但这一特性提供了一个方便的调试工具，可以用来查看代码中发生了什么。然而，如果视频代码占用了所有的处理器能力和内存，那就没有什么意义了。另一方面,[Dave]的视频输出程序只占用 1200 字节的 ram 和 24%的处理器，用于 VGA 上的 50×18 文本显示，为您需要微型板做的任何事情留下了大量空间。

在如此小巧轻便的设备上输出视频是一项令人印象深刻的壮举，尤其是在为其他任务节省空间的同时。这使它坚定地走出新奇的领域，进入有用工具的空间。然而，如果你想在一次中尝试同样的事情，你可能必须想出一些更令人印象深刻的技巧。

 [https://www.youtube.com/embed/5UFpp3ao460?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5UFpp3ao460?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

