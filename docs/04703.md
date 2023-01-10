# 谷歌创造可调试的 IPhone

> 原文：<https://hackaday.com/2019/11/03/google-creates-debuggable-iphone/>

苹果因许多事情而闻名，但向世界开放他们的平台不是其中之一。根据[Brandon Azad]最近在谷歌上发表的一篇文章，确实存在为开发 JTAG 端口和其他神奇功能而制造的[特殊 iphone](https://googleprojectzero.blogspot.com/2019/10/ktrw-journey-to-build-debuggable-iphone.html)。该端口在所有的 iphone 中都是[(虽然没有人使用)，但是默认情况下是锁定的。我们不知道要得到一部神奇的 iPhone 需要什么，但我们猜测谷歌不会把机顶盒送给三位 Macbook 专业人士，让他们进入等待名单。但是锁定的东西可以解锁，[布兰登]着手打造一款可调试的 iPhone。](https://www.theiphonewiki.com/wiki/Baseband_JTAG)

利用一些调试寄存器，可以在 A11 CPU 执行的任何时候对其进行调试。[Brandon 的]工具单步执行系统重置，并在关键指令后对 CPU 进行一些修改，以防止内核内存锁定。之后，世界就是你的了。KTRW 是使用这种技术构建的工具，可以用标准电缆调试 iPhone。

这个名字是 KTRR 上的一个剧本，KTRR 是内核文本只读区。这项工作效仿了一些做类似事情的早期开发。然而，这些方法没有 KTRW 提供的灵活性。

老实说，我们真的不关心调试 iPhone，但如何绕过所有苹果保护的猫和老鼠的故事是一个很好的阅读。当然，这真的是猫和老鼠。KTRW 不能在 A12 设备上工作。奇怪的是，[布兰登]认为其他人已经知道这种或类似的方法来破坏手机，但没有公布它来阻止苹果关闭让他们进来的门。

苹果手机以安全著称，但它们确实遭到黑客攻击。如果你想让其中一些失效，你只需要[一个儿童气球](https://hackaday.com/2018/10/31/helium-can-stop-your-iphone-maybe-other-mems-too/)。