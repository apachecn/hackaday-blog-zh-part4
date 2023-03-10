# tens flow lite-on command 64 的作用

> 原文：<https://hackaday.com/2022/07/06/tensorflow-lite-on-a-commodore-64/>

TensorFlow 是一个机器学习和人工智能库，它实现了如此多的功能，并将人工智能带到了大多数开发人员的能力范围内。但公平地说，它不适合功能较弱的计算机。对于他们来说，有 TensorFlow Lite，其中一个模型是在一个更大的机器上创建的，并导出到一个微控制器或类似的资源受限的机器上。[Nick Bild]可能将这一点发挥到了极致，在 Commodore 64 上实现了这一壮举。不仅如此，他还使用 Commodore BASIC 完成了这项工作。

TensorFlow Lite 的工作原理是将模型创建为 C 数组，然后由微控制器上的解释器对其进行解析和运行。这有点超出了 mighty 64 的能力，因此他创建了一个 Python 脚本来完成解释器的工作，并生成可以在 64 上运行的 Commodore 基本代码。值得信赖的 Commodore 是当时功能更强大的家用电脑之一，但我们相当肯定，它的设计者做梦也没想到它能做到这一点！

如果您有兴趣了解更多关于 TensorFlow Lite 的信息，[我们已经在过去的](https://hackaday.com/2017/11/23/smarter-phones-in-your-hacks-with-tensorflow-lite/)中讨论过了。

表头:MOS6502， [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:Commodore_C64_Tastatur_Links.jpg) 。