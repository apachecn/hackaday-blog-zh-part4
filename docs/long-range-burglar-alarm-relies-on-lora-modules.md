# 远程防盗报警依赖于 LoRa 模块

> 原文：<https://hackaday.com/2022/01/28/long-range-burglar-alarm-relies-on-lora-modules/>

【精英虫】出了问题；仓库发生了两起轻微的盗窃案。该单位有厚厚的混凝土墙，手机信号很差，而且不可能永久布线。因此，他着手研究一种能够满足他独特需求的防盗报警器。

ESP32 是操作的核心，与运行在 868 MHz 的远程 LoRa 无线电模块配对。与 4G、5G 或 WiFi 等高频技术相比，这种较低的频率在厚壁中具有更好的穿透力。随着一个小线圈天线伸出 3D 打印外壳的顶部，当存储单元被非法访问时，该设备能够很容易地与[Elite Worm]通信。

考虑到安全性，该设备不只是警告开门事件。如果存储单元中的远程发射器失去信号，可能是由于高级对手切断电源，也将发出警报。不过，在发射器方面还有一些工作要做，因为[精英蠕虫]需要确保门传感器在所有情况下都是可靠的。

许多人将他们的硬件技能用于安全服务，[我们经常看到有进取心的黑客修改专有的警报系统。休息后的视频。](https://hackaday.com/2019/04/27/this-owner-took-control-of-their-proprietary-alarm-system/)

 [https://www.youtube.com/embed/LClwDKtO31o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LClwDKtO31o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

