# Gameslab:另一个 FPGA 游戏控制台徽章

> 原文：<https://hackaday.com/2019/12/06/gameslab-the-other-fpga-game-console-badge/>

任何到过 Supercon 的人无疑都会记得挂在每个人脖子上的徽章。有些是合理的，而有些是脖子紧张的怪物，添加任何东西和一切黑客徽章到一些很酷的东西。我们看到从人工智能相机到全自动驾驶汽车的一切都被自豪地穿着。

遗憾的是，我们错过了一款基于 FPGA 的便携式游戏机[gamelab](https://craigjb.com/2019/11/26/gameslab-overview/)。不，不是[那种基于 FPGA 的游戏主机](https://hackaday.com/2019/11/04/gigantic-fpga-in-a-game-boy-form-factor-2019-supercon-badge-is-a-hardware-siren-song/)；在一个英雄所见略同的例子中，[克雷格]实际上已经玩弄他自己的掌上游戏机设计很长一段时间了。我们不得不说结果是惊人的。

其核心的 FPGA 是 Xilinx Zynq FPGA-ARM Cortex A9 combo SoC，通常是一种昂贵得令人望而却步的芯片。当[Craig]在易贝发现“翻新”的 Zynq 芯片，其价格不到新设备价格的 10%时，这实际上是游戏的开始。该控制台需要一个六层 PCB 来支持大型 BGA 芯片及其周围的数百个支持组件。有一个 5 英寸的 TFT 触摸屏，在 FPGA 中实现了视频控制器，一个立体声音响系统，以及你在现代控制台上期望的所有按钮和拇指棒。

对于我们的钱，最好的部分是案件，其中[克雷格]尚未分享任何细节。但它看起来像一个加工过的铝板，每个切口周围都有宽倒角，与刷过的表面形成鲜明对比。我们将期待更多的细节和游戏实验室的进展。