# Luxmeter 遇上 Linux

> 原文：<https://hackaday.com/2019/04/11/luxmeter-meets-linux/>

在过去的 30 年里，硬件的价格缓慢但稳定地下降，现在可以在网上买到各种各样的小配件和小发明，价格比一顿意大利大餐还低。总的来说，这是一件好事，但是发现您的新工具被软件方面的事情所拖累并不罕见。当然，你总是可以开发你自己的解决方案——[,在[ThePhil]的案例中，这正是他所做的。](https://github.com/philpagel/PCE174-communication)

有问题的硬件是 PCE-174 勒克斯计，它带有一个不合作的 Windows 应用程序作为标准。这根本不行，所以[ThePhil]开始用 Python 开发 Linux 版本。这是通过文件的帮助实现的，不是 PCE-174，而是另一家公司的兄弟 Extech HD450。这两个仪表非常相似，以至于 Extech 更好的文档能够填补[ThePhil]理解上的空白。

[ThePhil]努力实现了 PCE-174 的全部功能，并很好地记录了该项目。甚至还有关于各种依赖项的版本号的注释，如果有人试图在五年后运行代码，这肯定会是一个很大的帮助。

这是一个很好的教训，一个人不需要受软件的支配。在很多情况下，你可以推出自己的健壮的解决方案，并完成工作。这种方法可以很长——[如果你愿意，你甚至可以更换整个相机固件。](https://hackaday.com/2015/04/04/magic-lantern-brings-linux-to-canon-eos-cameras/)