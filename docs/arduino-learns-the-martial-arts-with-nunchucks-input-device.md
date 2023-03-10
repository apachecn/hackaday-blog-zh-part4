# Arduino 用双截棍输入设备学习武术

> 原文：<https://hackaday.com/2021/01/26/arduino-learns-the-martial-arts-with-nunchucks-input-device/>

每堂计算机入门课都有一个令人厌烦的部分，展示计算机是如何由输入、输出和处理组成的。也许输入设备是双截棍就不会这么无聊了。[【Brian Lough】是这样认为的，他挑衅地宣称双截棍是有史以来最好的输入设备](https://www.youtube.com/watch?v=Cl9f1DUbMnc)。通过与 Wii 控制器和相关库的简单连接，您可以访问模拟操纵杆、两个按钮和一个加速度计。

双截棍是用来插入 Wii 控制器的，连接是 I ² C，所以与 Arduino 或其他小型微控制器的接口很简单。唯一的问题是建立联系。我们可能只是剪断了电线，但[Brian]更喜欢使用一个小型分线板，它可以插入到库存连接器中，并为您自己的电缆提供焊点。分线板有多种选择，而[Brian]有他自己的设计，你可以从 OSHPark 以大约 1 美元的价格买到 3 块板。你也可以直接把电线塞进连接器，但这并不总是可靠的。

控制器使用 3.3V，这在当今并不罕见。有一个图书馆可以方便阅读。显然，并不是所有的应用程序都适合，但我们确实喜欢[Brian]开发的俄罗斯方块游戏。这对于任何类型的运动控制也是很自然的，比如他的万向架例子。

即使你没有垃圾 Wii 控制器，它们在转售市场上也很常见，你不用花太多钱就能买到新的第三方控制器。让我们很抱歉上次搬家时扔掉了我们的。

如果你想玩双截棍，你可以[全定制](https://hackaday.com/2020/04/26/custom-bluetooth-joystick-in-a-nunchuk-shell/)。或者，干脆放弃，把一个变成[树莓派](https://hackaday.com/2019/05/13/wii-nunchuk-gets-a-built-in-raspberry-pi-zero/)。

 [https://www.youtube.com/embed/Cl9f1DUbMnc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Cl9f1DUbMnc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

