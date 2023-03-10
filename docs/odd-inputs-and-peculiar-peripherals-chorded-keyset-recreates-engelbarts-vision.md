# 奇怪的输入和特殊的外设:和弦键盘再现恩格尔巴特的视觉

> 原文：<https://hackaday.com/2022/06/26/odd-inputs-and-peculiar-peripherals-chorded-keyset-recreates-engelbarts-vision/>

道格拉斯·恩格尔巴特 1968 年的《所有演示之母》向世界介绍了我们今天视为理所当然的一系列技术，其中最突出的是他的伟大发明——电脑鼠标。然而，MOAD 也展示了诸如剪切粘贴文本编辑，点击界面，视频会议，甚至在线协作 *à la* Google Docs。其中一项创新显示，出于某种原因，和弦键盘没有经受住时间的考验:这是一种带有五个键的输入设备，可以以不同的组合同时按下，就像你在钢琴上弹奏和弦一样。

[![A 3D-printed five-key chorded keyboard](img/064a68e2b1228ce7d8688e3984c46e61.png)](https://hackaday.com/wp-content/uploads/2022/06/Engelbart-Keyset-side.jpg)

The Engelbart Keyset comes with both USB host and USB client ports

虽然这些年来已经进行了一些尝试来给“chorder”带来新的生命，但它未能获得主流的吸引力，直到今天仍然是一种好奇。这使得它非常适合参加*奇怪的输入和特殊的外围设备*比赛，正如我们在【Russ Nelson】提交的名为 [Engelbart Keyset 的作品中看到的那样，该作品旨在创建一个现代 3D 打印和弦，完全按照 Engelbart 的意图工作](https://hackaday.io/project/185908-engelbart-keyset)。

重要的是要注意和弦键盘并不意味着只是一组额外的五个键。相反，Engelbart 展示了 chorder 和鼠标之间的巧妙相互作用:他左手下面的五个键和右手下面的三个鼠标按钮可以组合起来，创建一个完整的 8 位输入设备。因此[Russ]的设备包括一个连接 USB 鼠标的 USB 主机接口以及一个 USB 客户端接口，它将自己作为一个组合鼠标/键盘设备呈现给 PC。

该设备的大脑由一个 Teensy 4.1 组成，它读出鼠标发送的代码以及顶部的五个键。如果这些键中的一个或多个与鼠标按钮一起被按下，则生成对应于 Engelbart 的原始键码映射的键盘码。我们想知道这整个系统在现实生活中有多实用；这看起来像是你必须亲自尝试才能发现的东西。幸运的是，所有的原理图、代码和 STL 文件都可以在项目页面上找到，所以只需一点点工作，你就可以在你的办公桌上拥有自己的 MOAD 设置。

我们在这些页面上展示了几个和弦键盘；脑海中浮现出[微微和弦](https://hackaday.com/2022/05/06/pico-chording-keyboard-is-simultaneously-vintage-and-new/)、[和弦](https://hackaday.com/2021/08/30/chordie-chording-keyboard-speaks-no-qwerty/)和[球棒](https://hackaday.com/2020/08/18/inputs-of-interest-the-infogrip-bat-chording-keyboard/)。如果你想重温恩格尔巴特令人惊叹的演讲，可以看看我们的[所有演示之母](https://hackaday.com/2019/01/03/retrotechtacular-the-mother-of-all-demos-50-years-on/)50 年。

[![Odd Inputs and Peculiar Peripherals Contest](img/4c1d0cbefc0219866bf706dbbac40818.png)](https://hackaday.io/contest/185414-odd-inputs-and-peculiar-peripherals)