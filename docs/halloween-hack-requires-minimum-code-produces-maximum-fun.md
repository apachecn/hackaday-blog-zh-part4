# 万圣节黑客需要最少的代码，产生最大的乐趣

> 原文：<https://hackaday.com/2021/11/07/halloween-hack-requires-minimum-code-produces-maximum-fun/>

每年，[康纳·奥尼尔]都会做些东西来吓唬和娱乐那些在万圣节来到他家的“不给糖就捣蛋”的人。他注意到了一种模式——每年项目都包含大量代码，通常是使用不同的框架和语言拼凑起来的。为了缓解这种情况，并使事情变得对初学者更友好一些，可以理解，初学者会发现代码密集型项目令人望而生畏，今年他开始尽可能少写代码。

没有走纯电子路线，这无疑包括几个 555 定时器和一些其他经典产品， [[Conor]选择坚持使用更高级别的嵌入式主板，包括粉丝最喜欢的 ESP32 和 Raspberry Pi，同时仍然试图将代码保持在最少。](https://conoroneill.net/2021/11/01/no-code-halloween-hacking-with-blockly-espruino-node-red-tines/)多亏了可视化语言 Espruino Blockly 和 NODE-RED，他只需要写几行他称之为“传统代码”的代码:一个简单的 JavaScript HTTP 请求。该项目本身由一个连接到 ESP32 的超声波传感器组成，它可以检测到孩子何时靠近门。ESP32 使用 Espruino 可视化脚本在感应到运动时通知 Raspberry Pi。树莓派会播放一些怪异的声音，配合一些旧的会议徽章，打开一些灯，触发一台造雾机。Pi 还使用一种叫做[的服务通过电报发送上门通知。](https://www.tines.com/)

好的，这仍然不简单，但是有趣的是不用写太多代码就可以做很多事情(最终结果很棒！).[Conor]说他在过去十年左右的时间里每年都在建造类似的万圣节项目，它显示了— [我们在 2015 年写了他的另一个闹鬼的门铃](https://hackaday.com/2015/11/14/halloween-doorbell-prop-in-rube-goldberg-overdrive/)。我们期待着明年看到他做的东西，我们希望你也能有一些令人敬畏的自动化万圣节装饰品！

 [https://www.youtube.com/embed/i8a4AJPny50?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/i8a4AJPny50?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

