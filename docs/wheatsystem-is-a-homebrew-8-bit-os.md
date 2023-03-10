# WheatSystem 是自制的 8 位操作系统

> 原文：<https://hackaday.com/2022/10/14/wheatsystem-is-a-homebrew-8-bit-os/>

【Esperantanaso】长期参与生产家酿 8 位电脑。他的各种构建都可以实现不同的东西，但他对为一个构建的应用程序不能在另一个上轻松运行感到沮丧。不过，他最近在这一领域取得了巨大的进步，发明了自己的 8 位操作系统 WheatSystem。

这项工作最初从 BreadSystem 开始，它依赖于字节码中存在的应用程序。这将由 BreadSystem 操作系统运行，操作系统将处理必要的转换，将其转换为运行它的系统的机器代码。然而，在实现文件系统和浮点处理等高级功能时，工作很快就失去了控制。BreadSystem 看起来可能太重，无法在轻量级 8 位系统上运行。

这导致了 WheatSystem 的开发，它保留了来自 BreadSystem 的字节码运行时环境、统一堆和内存许可系统。精细的内存许可、自动垃圾收集和文件系统目录等更好的特性被放弃了。

WheatSystem 很快成为一个基本的功能性操作系统。为了证明这一点，[Esperantanaso]创造了一台基于 ATmega328 的小型自制电脑 [WheatBox 55A1](http://ostracodfiles.com/wheatbox55a1/main.html) 。它很容易运行简单的应用程序，如素数生成器或基本的 RPG。

创建自己的操作系统绝非易事，即使是在 8 位级别。我们在之前见过这样的事，它总能给人留下深刻印象。

 [https://www.youtube.com/embed/w8nGcwWr0XE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w8nGcwWr0XE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

