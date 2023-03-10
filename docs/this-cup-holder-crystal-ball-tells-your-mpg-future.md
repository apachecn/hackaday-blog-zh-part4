# 这个杯架水晶球告诉你 MPG 的未来

> 原文：<https://hackaday.com/2018/11/01/this-cup-holder-crystal-ball-tells-your-mpg-future/>

混合动力汽车越来越普遍，这种汽车将环保电动马达和汽油发动机结合起来，以扩大行驶里程。它们是一种过渡技术，提供了纯电动汽车的大多数优势，但没有电动汽车所有权的“可怕”元素，这些元素对消费者来说仍然是陌生的，例如在家里安装充电器。但是混合动力车仍然缺乏的一个要素是一个很好的方法来告诉司机他们是在使用石油还是锂；一眼就能看出他们的驾驶有多“环保”的方法。

[![](img/375f84a3d08d306779cd3b462f5fe791.png)](https://hackaday.com/wp-content/uploads/2018/10/ecorb_detail1.jpg) 【本·科林】和他的女儿【艾丽莎】想出了一个聪明的办法，允许改装现有的混合动力汽车，配备一个极其容易理解的实时汽车效率指标。没有令人困惑的图形或街机风格的哔哔声和 bloops，只有一个生活在杯架上的变色球。一个进化版本，它采用了一个较小的“顶灯”的形式，位于仪表板顶部，可能是混合动力市场上一个引人注目的售后配件。

这种被他们称为 ecOrb 的设备依赖于混合动力汽车的一个有趣的特性。用于现代车辆诊断的 OBD II 界面显然只显示混合动力汽车中汽油发动机的转速。因此，如果汽车在运动，但 OBD 端口报告 0 转/分，车辆必须在电力下运行。

通过将蓝牙 OBD 适配器插入汽车，所有[Ben]和[Alyssa]需要的是一个带有 HC-05 模块的 Arduino Nano 克隆体，以实时读取当前的推进模式。通过一些相当简单的条件逻辑，他们能够根据车辆的运行情况控制 RGB LED 的颜色:绿色代表电力驱动，紫色代表天然气驱动，红色代表天然气发动机怠速时(混合动力汽车的最差情况)。

如果你想了解更多关于这种快速发展的汽车的可能性，请查看我们之前对凯迪拉克 ELR 混合动力车的报道

 [https://www.youtube.com/embed/-JtqhXix-m8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-JtqhXix-m8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

