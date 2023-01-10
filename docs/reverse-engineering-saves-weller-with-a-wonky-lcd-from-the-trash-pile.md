# 逆向工程用垃圾堆里一个摇摇晃晃的液晶显示器拯救了韦勒

> 原文：<https://hackaday.com/2022/12/25/reverse-engineering-saves-weller-with-a-wonky-lcd-from-the-trash-pile/>

没有什么比在垃圾中找到一个坏掉的齿轮并让它复活更令人满意的了。令人满意，但也可能更耗时——毕竟，有人扔掉它是有原因的。找出原因并找到更好的支持方法是乐趣所在，也是危险所在。

幸运的是，一些设备具有相对较短的已知故障模式列表，这是[Lauri Pirttiaho]为[修复旧威勒 WD1 焊接站](https://hackaday.io/project/188741-replacing-broken-lcd-of-weller-wd1)所依赖的事实。该单位，体育熟悉的浅蓝色韦勒制服和一些划痕和丁，有一个液晶显示器是 DOA。通常是驱动程序出了问题，但是[Lauri]的诊断显示是 LCD 模块本身出了问题。

由于 OEM 替代品在这一点上基本上是不可获得的，修复方法是截取从驱动程序到旧 LCD 的数据标题，并将其发送到一个新的、容易获得的 16×2 字符 LCD 显示器。首先要检查显示控制器的数据表，并对旧显示器进行一些探查，以找出哪些段和背板映射到哪些引脚。一点点的外壳改造让新的显示器适合，旧的控制器芯片被移除，一个 PIC16 进入了它的位置，在一个整洁的 Kapton 胶带和 bodge 电线的巢中。PIC 的工作是将原始显示(有相当数量的自定义图标和符号)翻译成合理的基于文本的对等物，并通过 I2C 将它们发送到 16×2。下面的视频展示了黑客的行动；老实说，它看起来像是从工厂出来的。

这里好的一面是[Lauri]的修复方法适用于整个 Weller 站的范围，所以如果你在垃圾桶里找到一个，你也许能让它复活。如果做不到这一点，你可以(或多或少)从头开始打造自己的 Weller。

 [https://www.youtube.com/embed/9AM5GWSbaP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9AM5GWSbaP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

