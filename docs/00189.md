# 针对混合信号微控制器的旁路攻击

> 原文：<https://hackaday.com/2018/07/30/side-channel-attacks-against-mixed-signal-microcontrollers/>

你不应该通过蓝牙传输加密密钥，但这正是一些流行的无线微控制器已经在做的事情。这是 EUERCOM 的研究人员发表的一项研究成果“尖叫频道”背后的想法，并将在下周的黑帽大会上发表。到目前为止，研究人员已经调查了对支持蓝牙的微控制器的侧信道攻击，允许他们在受控环境中从 10 米远的地方提取 tinyAES 密钥。[论文的 PDF 可用](http://s3.eurecom.fr/docs/ccs18_camurati_preprint.pdf)，所有相关代码可从[的 GitHub](https://github.com/eurecom-s3/screaming_channels) 上获得。

这种利用的实验设置包括一个 [BLE 纳米](https://redbear.cc/product/ble-nano-kit-2.html)，一个北欧 nRF52832 蓝牙微控制器的分线板，一个 Hack RF，一个来自 Ettus 的 [USRB N210](https://www.ettus.com/product/details/UN210-KIT) 软件定义无线电，以及一些高增益天线和 lna。示例攻击依赖于在 BLE Nano 上安装固件，该固件通过几个循环运行，并用 tinyAES 加密某些东西。通过非常仔细地分析 RF 频谱，可以从以太中提取 AES 密钥。

近年来，旁道攻击受到了更多的关注。曾经只限于三个字母的机构级别的 Van Eck phreaking 现在可以廉价地在一个系统中完成，该系统有像 ChipWhisperer 这样的设备。

当然，这只是一个演示，说明在高度受控的环境中，侧信道攻击可能会发生什么，因为微控制器上运行的固件需要做大量工作。这并不能证明戴着巴拉克拉法帽的黑客正在穿过停车场嗅探你的手机，以获取你的 Instagram 账户的密码，但它确实显示了相对便宜的现成硬件的可能性。