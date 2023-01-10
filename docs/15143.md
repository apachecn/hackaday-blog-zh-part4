# 反编译软件修复旧太阳能逆变器

> 原文：<https://hackaday.com/2022/10/20/decompiling-software-to-fix-an-old-solar-inverter/>

电子设备几年后就会过时，这是不争的事实。有时这是因为技术在进步，但也可能是因为原始制造商不再支持它，一个功能完善的设备变得几乎无用。当[Buy It Fix It]发现一对二手 Power-One Aurora 太阳能逆变器时，他遇到了一个问题，他需要访问服务菜单，而这个菜单碰巧有密码保护。原来的制造商已经不复存在，品牌名称的当前所有者也无力提供帮助，因此[Buy It Fix It]不得不求助于[逆向工程来找到密码](https://www.youtube.com/watch?v=aOrd-1YLyKk)。

多亏了互联网档案馆的 Wayback 机器，[Buy It Fix It]才能够下载最初与逆变器一起提供的 PC 软件包。但是为了访问所有功能，需要一个密码，该密码只能通过向制造商注册该单元来获得。这是不会发生的，所以[购买它修复它]启动了 dnSpy，一个反编译器和调试器。NET 程序。经过一番搜索，他找到了检查密码的部分，只需将该部分复制到一个新程序中，他就能制作自己的密钥生成器。

现在有了服务密码，[Buy It Fix It]就能够将逆变器设置为正确的电压，并将其连接到他的太阳能电池板上。有趣的是，程序代码在很多地方也提到了“乓”、“俄罗斯方块”和“提拉米苏”；这些原来是代码中的复活节彩蛋，包含这两个游戏的简单版本以及一张意大利甜点的照片。

在软件档案中还有另一个程序，可以对逆变器内部的低级功能进行编程，很少有用户需要接触这些功能。这个程序不是用。但是在 C 或类似的语言中，所以它需要使用 x32dbg 来查看机器码。同样，这个程序是有密码保护的，但是主密码只是以未加密字符串“91951”的形式存储，即制造商旧电话号码的最后五位数字。

当[购买它修理它]第一次得到它时，逆变器实际上并没有工作，如果你对电力电子维修感兴趣，他的维修视频(也嵌入在下面)也很值得一看。黑掉太阳能逆变器[来实现更多功能](https://hackaday.com/2017/01/27/solar-controller-reverse-engineered-in-both-directions/)通常是可能的，但是当然如果[整个设计是开源的](https://hackaday.com/2016/07/10/open-source-solar/)就容易多了。

 [https://www.youtube.com/embed/aOrd-1YLyKk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aOrd-1YLyKk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/NSEy6JwYGtw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NSEy6JwYGtw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

