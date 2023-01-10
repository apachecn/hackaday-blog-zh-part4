# 用这个蓝牙击键注入器注入你喜欢的任何击键

> 原文：<https://hackaday.com/2019/12/03/inject-keystrokes-any-way-you-like-with-this-bluetooth-keystroke-injector/>

[Amirreza Nasiri]送来了这个很酷的 [USB 击键注射器。](https://github.com/AmirrezaNasiri/usb-keystroke-injector)

该设备由 Arduino、蓝牙模块和 SD 卡组成。当它插入目标计算机时，该设备从 SD 卡加载选定的有效载荷，从而危及系统。然后，它做它独特的把戏，将注射器切换到蓝牙模式。现在攻击者对系统有了更多的控制，尽管是在本地。

虽然我们从未想过将这款设备插入真正的计算机，但我们喜欢一些额外的功能，如如何根据所需的攻击，使用额外的 dip 开关来选择多达 8 种不同的有效载荷。增加一个[光电二极管](https://hackaday.com/2019/02/22/radiation-detector-eschews-tubes-uses-photodiode/)也很有趣，让我们梦想各种不切实际的电影黑客场景。[Amirreza]说它会在人离开房间关灯时触发。

[Amirreza]在 GitHub 上有所有的代码和设计文件。还有一些有效载荷的例子，应该很有趣。毕竟，生活的乐趣之一就是寻找新的方法来和你的朋友们搞在一起。