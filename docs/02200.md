# 保护良好的 USB 电源板使其易于插入

> 原文：<https://hackaday.com/2019/02/24/well-protected-usb-power-strip-makes-it-easy-to-plug-in/>

当我们这些天得到一个新设备时，包装中的某个地方很可能是一个壁式 USB 电源。我们寻找一个地方来插入小开关模式的转换器，重新安排电源接线板上的几个插头，并诅咒它的设计师过于舒适的插座间距。与此同时，电源线上的 USB-A 插头以其整洁、紧凑的外形嘲弄着我们。要是有 USB 插线板就好了。

不愿意再忍受这样的侮辱，[斯科特·m·贝克]自己动手设计了这个 USB 配电系统。我们很惊讶地听说，他无法找到一个商业 USB 电源条，但即使他有，它可能不会有他添加到他的铃铛和口哨。该电路经历了几个版本，但每个版本都专注于保护连接的 USB 设备。他在 TPS2421 热交换控制器周围构建了电子保险丝形式的过流保护，并使用带有常见齐纳-SCR 配置的撬棍电路提供过压保护。还有一个瞬态电压抑制二极管，以防止任何电感尖峰。有趣的是，每个 USB 插座都有所有这些保护——它不仅仅是一条受保护的总线并行为一堆 USB 插座供电，而是具有所有电路的单个模块。这些模块可以组合在一起，放在一个激光切割的亚克力盒子里。下面的视频详细展示了设计和构建过程。

不得不说，我们总是从[Scott]的项目中学到很多关于电路设计的东西。你可能会想起[他定制的雅达利 2600 控制器](https://hackaday.com/2018/08/08/thumbs-up-for-this-custom-atari-5200-controller/)或者[他的双端口记忆复古游戏控制台](https://hackaday.com/2018/07/26/dual-port-memory-and-raspberry-pi-team-up-for-retro-console-multicart/)，这两个产品本身就很有趣，也很有教育意义。

 [https://www.youtube.com/embed/TfDImaxxth0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TfDImaxxth0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

