# 946C 热板控制器增加了 BLE 回流曲线上传

> 原文：<https://hackaday.com/2022/09/30/controller-for-946c-hotplate-adds-reflow-profile-upload-over-ble/>

如果你能保持你的设计单面，回流加热板是 PCB 组装的一个极好的工具。特别是 946C 热板已经引起黑客的注意有一段时间了——一个 200x200mm 毫米的工作表面热板售价不到 100 美元，是一笔不错的投资。与其他回流工具一样，有人为它制作替代控制器只是时间问题。这一个，你会想要记住——它是[Arnaud Durand]和[Elias Rodriguez Martin]的替代控制器项目,叫做 Reflow946。

按照最佳实践，该板是库存控制器的简易替代品，只需更换电缆即可。主机处理器是一个 ESP32，它允许您在 Python 应用程序的帮助下，使用 BLE 对回流曲线进行编程。[整个设计是开源的，在 GitHub 上，](https://github.com/DurandA/reflow946/)当然，保持最好的 3D 打印传统，你已经可以订购零件和 PCB，然后使用你即将升级的热板组装它们。就售后市场控制器而言，毫无疑问，该板可以让您更好地控制回流，并允许您补偿任何可能的低于标准的校准。

![Picture of the hotplate of the kind that this controller board is aimed at.](img/1e0635789c65d5127e85aca4fbac059a.png)由于热板的外壳是金属的，【Arnaud】推荐一个带有外部天线连接器的 ESP32 模块。您还需要注意兼容性-事实证明，只有一些作为 946C 出售的电炉适合此主板，所以如果您打算购买能够进行此升级的电炉，请与您的卖家联系。几乎让我们希望这些烤箱有修订号，也许型号后面有个字母什么的！

一段时间以来，热板回流一直是我们最喜欢的 PCB 组装方法之一，hacker 的独创性为我们提供了不同的方法——装满沙子的[煎锅](https://hackaday.com/2019/06/05/solder-smds-with-a-pan-o-sand/)、[平面 PTC 加热器、](https://hackaday.com/2016/05/21/ptc-heaters-for-reflow-soldering/)甚至是设计用于回流 PCB 的[PCB。](https://hackaday.com/2021/10/06/using-a-pcb-to-reflow-pcbs-take-2/)还不熟悉回流是什么意思？[让我们来帮你加速吧！](https://hackaday.com/2016/06/02/tools-of-the-trade-reflow/)

我们感谢[Abe Connelly]与我们分享这些！

> 使用 [#ESP32](https://twitter.com/hashtag/ESP32?src=hash&ref_src=twsrc%5Etfw) 为 946C 热板开源[#蓝牙](https://twitter.com/hashtag/Bluetooth?src=hash&ref_src=twsrc%5Etfw)回流控制器。这个控制器取代了原来的电路板。https://t.co/zbGDrLhWYW[pic.twitter.com/iHjVU38IiW](https://t.co/zbGDrLhWYW)
> 
> —阿诺·杜兰德(@杜兰达 23)[2022 年 9 月 20 日](https://twitter.com/DurandA23/status/1572284470044106752?ref_src=twsrc%5Etfw)