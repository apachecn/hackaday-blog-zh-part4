# 使过时的电动汽车充电站现代化

> 原文：<https://hackaday.com/2022/06/12/modernizing-an-outdated-electric-vehicle-charging-station/>

作为早期采用者的一个缺点是，你可能最终投资于很快就会过时的设备。尽管很明显电动汽车将继续存在，但那些几年前为电动汽车购买充电站的人可能会发现它速度慢，与现代汽车或计费网络不兼容，因此需要升级到最新型号。

如果你不介意修补，这些旧充电器可以为你建造自己的最先进的充电站提供一个极好的基础，就像《极客日记》的[詹姆斯]所做的那样。他买了一个 Chargepoint CT2000 系列充电器，[在里面安装了一个全新的基于 OpenEVSE 组件的充电单元](https://diary-of-a-geek.blogspot.com/2020/09/openevse-chargepoint-evse-ct2000.html)。CT2000 是一款已经停产的老款产品，虽然它仍然可以连接到 Chargepoint 的网络，但续费需要几千美元。[James]不愿意为一个无论如何都要安装在家里的装置投资，所以他决定从 OpenEVSE 购买替换零件，open evse 是一家开源电动汽车充电站和组件的供应商。

[![An OpenEVSE controller mounted on a bracket](img/42152c84bc0ae10e63685a94e8d8b35c.png)](https://hackaday.com/wp-content/uploads/2022/06/OpenEVSE-Controller.jpg)

The OpenEVSE charging controller sitting on the ChargePoint bracket

充电站的内部实际上非常简单，因为真正的电池充电器在汽车内部:充电站只包含一个强大的接触器来开关交流电流，以及一些测量电流的电路和一个连接到某种支付网络的接口。因此，第一步是将接触器和电流互感器连接到 OpenEVSE 控制器。这很容易，因为新零件比原来的小得多，可以简单地安装到现有的支架上。

第二步是提供用户界面和网络连接。[James]将显示器和无线系统从主机上拆下，并在前面切了一个大洞，为新的 LCD 显示器提供空间。一组状态 led 加上 WiFi 连接完善了这个系统，现在看起来和原来一样专业。测试表明，液晶显示器在明亮的阳光下很难阅读，所以[James]用有机发光二极管显示器取代了它们，但除此之外，翻新的充电站工作得非常好。

当然，在高电压和大电流下工作需要适当的技能和工具，而[詹姆斯]显然拥有这些；他还强调了在任何户外设备中安装接地故障断路器的重要性。他也不是唯一一个建造自己充电站的人。如果你对多种类型的电动汽车充电连接器感到困惑，看看[我们最近的一篇描述所有这些不同插头和插座的文章](https://hackaday.com/2022/04/28/ev-charging-connectors-come-in-many-shapes-and-sizes/)。谢谢你的提示，[凯文]！