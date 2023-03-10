# DIY USB 麦克风似乎有些矫枉过正；非常深入

> 原文：<https://hackaday.com/2021/06/02/diy-usb-microphone-seems-overkill-is-surprisingly-in-depth/>

我们这些过去一年一直在家通过视频电话工作的人可以证明，对网络摄像头和麦克风等会议设备的需求正在上升。不想跳出来一个无聊的现成解决方案，连环黑客【安迪·布朗】决定[从头开始设计自己的 USB 解决方案，并向我们展示了从开始到结束的过程](https://andybrown.me.uk/2021/03/13/usb-microphone/)。

决定对电路进行全数字设计，外设基于 MEMS 麦克风和 STM32 微控制器，在它和 USB 连接之间承担重任。[Andy]注意到 MEMS 麦克风非常脆弱，必须在声音进入的孔周围设计 PCB，这就是为什么他选择了一个分线板，上面已经焊接了元件。

至于 MCU，他的理由是，由于这是一个一次性的项目，不会大量生产，180 MHz 的 ARM 内核不应该被视为矫枉过正，因为它也给他足够的空间来处理信号，使声音更清晰，然后通过 USB 音频设备描述符发送到计算机。

选择好元件和设计好电路板后，[Andy]详细解释了他为 STM32 编写的固件，该固件将麦克风 I S 接口的 PCM 样本转换成更适合计算机的格式。他还描述了它如何处理音频，应用图形均衡器来降低噪声，然后是 ST 自己的智能音量控制滤波器，它更像一个压缩器，而不是简单的振幅乘法。

最后，该项目的所有文件，包括 board gerbers 和 STM32 固件，都可以在他的帖子底部找到，此外，还有一个演示该项目的视频，休息后可以在这里查看。鉴于他已经为 STM32 G0 系列制作了[自己的开发板，因此【Andy】选择微控制器用于这个项目对我们来说并不意外。但是如果这个数字麦克风项目对你来说有点太现代了，为什么不试试在](https://hackaday.com/2019/07/16/building-a-development-board-for-the-stm32-g0-series/)[制作一个带状麦克风](https://hackaday.com/2021/03/18/wooden-you-love-to-build-a-ribbon-microphone/)呢？

 [https://www.youtube.com/embed/61jC4nUQyDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/61jC4nUQyDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

