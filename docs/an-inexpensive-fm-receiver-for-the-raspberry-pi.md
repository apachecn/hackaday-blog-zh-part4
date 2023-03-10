# 树莓派的廉价调频接收器

> 原文：<https://hackaday.com/2021/09/07/an-inexpensive-fm-receiver-for-the-raspberry-pi/>

在这一点上，树莓派不乏令人印象深刻的黑客。[Dilshan Jayakody]最近记录了他为 Pi 平台设计和构建[廉价 FM 立体声接收机的经验，结果令人印象深刻。](https://hackaday.io/project/181563-fm-stereo-receiver-add-on-for-raspberry-pi)

相当多的 FM 接收机项目以 RDA5807 或 TEA5767 ICs 为中心，然而[Dilshan]在其构建中使用了 Quintic Corporation 的 QN8035。QN8035 与 Pi 的 I2C 总线接口只需在令人愉悦的单面 PCB 上安装少量分立元件。

在演示了 FM 调谐器可以在命令行进行调谐之后，[Dilshan]编写了一个智能的 GUI 应用程序，使调谐变得轻而易举。该软件允许收听者手动和自动扫描调频电台，解码节目服务数据，控制音量，并显示调谐器的 RSSI 和信噪比读数。

正如我们之前报道的,[调频广播正在慢慢走向淘汰](https://hackaday.com/2021/08/26/fm-radio-the-choice-of-an-old-generation/)。这个最新的项目并不旨在开辟新的领域，但是它的简单性和廉价的组件是初级黑客和无线电爱好者的完美结合。更多细节可以在 [Hackaday.io](https://hackaday.io/project/181563-fm-stereo-receiver-add-on-for-raspberry-pi) 上找到。原理图、源代码和物料清单可以在 [GitHub](https://github.com/dilshan/gtk-fm-radio) 上找到。

 [https://www.youtube.com/embed/qJ5dKJD2EvY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qJ5dKJD2EvY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

