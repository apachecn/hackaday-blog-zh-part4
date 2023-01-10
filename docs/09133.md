# 用 Arduino 升级旧 MIG 焊机送丝机

> 原文：<https://hackaday.com/2021/02/01/upgrading-an-old-mig-welder-wire-feeder-with-arduino/>

如果你预算有限，旧的工业设备通常是一个很好的选择，你甚至可以自己添加一些高级功能。[理论上可行]的[Brett]已经完成了他的旧 MIG 焊机，[在 Arduino](https://www.youtube.com/watch?v=DnUJ3-JhBJA)的帮助下增加了高级控制功能。

[Brett]追求的主要功能是前流、后流和点焊计时器。预流在填充焊丝通电前一刻开始保护气体的流动，而后流在焊接完成后保持气体流动。这减少了氧气污染焊缝的机会。点焊定时器自动限制焊接时间，实现一致和可重复的点焊。

Miller S-22A 送丝机可以具有这些特征，但是它需要昂贵且难以找到的控制单元。它所做的只是控制气流、电源和送丝机的继电器的激活时间，所以[Brett]决定使用 Arduino 代替。焊机控制电路在 24V 下运行，因此光隔离器接收触发信号，继电器用于输出。电位计被添加到原来的控制面板上，所有的线路都整齐地安装在它的后面。升级工作非常完美，并允许[布雷特]提高他的焊接质量。完整细节请看休息后的视频。

如果你愿意接受这种交换，逆变焊机可以以便宜得离谱的价格买到。我们也看到了一些其他的 DIY 焊机升级，在[小型](https://hackaday.com/2019/11/04/improbably-cheap-pocket-welder-gets-an-esp32-makeover/)和[大型](https://hackaday.com/2019/09/12/modified-tombstone-welder-contains-a-host-of-hacks/)机器上。