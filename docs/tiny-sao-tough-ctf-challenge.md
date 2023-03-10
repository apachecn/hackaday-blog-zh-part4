# 微小的骚，艰难的 CTF 挑战！

> 原文：<https://hackaday.com/2019/11/07/tiny-sao-tough-ctf-challenge/>

自 SAO 连接器规范发布以来的一两年里，我们已经看到了各种各样的子板，用于我们最喜欢的电子徽章。其中许多都是艺术作品，但还有另一个子集，远不是为了展示，而是为了巧妙的功能。[【Uri Shaked】的小骚](https://blog.wokwi.com/capture-the-flag-shitty-add-on/)看起来相当不好看，是一个小小的圆形 PCB，只有一个 ATtiny 微控制器，复位按钮，和孤零零的 LED，但它的兴趣不在于它的外观，而在于它的软件。它包含了一系列的 CTF 谜题，尽管它看起来很简单，但包含的内容应该足以拘留最顽强的解谜黑客。

这是一个由三部分组成的难题，在最简单的层面上，仅仅闪烁 LED 就足够了，而下一个层面涉及到从固件中检索隐藏的字符串，最后一个需要用自己的字符串替换字符串。您只能通过 SAO 连接器这样做，但幸运的是，您可以访问[源代码](https://github.com/urish/ctf-shittyaddon/blob/master/ctf-firmware/ctf-firmware.ino)来查找漏洞。很明显，微控制器的数据手册可能也很有用。

[Uri]已经在这些页面上出现了很多次，最近一次是他[给他的 3D 打印机](https://hackaday.com/2019/08/03/add-a-microscope-to-your-3d-printer/)添加了一个显微镜。