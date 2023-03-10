# 3D 打印机控制板包含一个 Raspberry Pi 计算模块 4

> 原文：<https://hackaday.com/2021/05/01/3d-printer-control-board-packs-a-raspberry-pi-compute-module-4/>

传统上，3D 打印机控制板使用简单的 8 位微控制器来命令步进驱动器，并最终将机器移动到它需要去的地方。较新的主板已经转向 32 位微控制器，但它们的计算能力仍然相对有限。正因为如此，运行 OctoPrint 的 Raspberry Pi 通常用于提供更复杂的功能，如远程管理和视频直播。

为了将这些不同的设备整合到一个一体化的主板中， [[pkElectronics]开发了 Sigmoid S7P](https://hackaday.io/project/179342-sigmoid-s7p-3d-printer-control-board) 。凭借 STM32 微控制器、TMC2209 步进驱动器、Raspberry Pi 计算模块 4 和充足的扩展空间，它有望成为任何运行在开源固件上并可移植的 3D 打印机的直接升级。

[![](img/ad821eb5bc01098535e4ff3f6306bb61.png)](https://hackaday.com/wp-content/uploads/2021/04/sigmoid_detail3.jpg)

An earlier concept for the Sigmoid

根据[pkElectronics]的说法，Sigmoid 的想法已经存在好几年了，但由于难以处理计算模块之前迭代使用的 SO-DIMM 接口，因此从未付诸实施。但是随着 CM4 的[切换到更小更密集的连接器，电路板终于开始成形。](https://hackaday.com/2020/10/19/new-raspberry-pi-4-compute-module-so-long-so-dimm-hello-pcie/)

无论你只是将它作为一种将 OctoPrint 集成到你的打印机的便捷方式，还是想让 T2 进入更高级的领域，如 Klipper T3，Sigmoid S7P 看起来都是一个非常令人兴奋的项目。[pkElectronics]表示，如果有兴趣的话，他们正在考虑商业化生产这种板，所以如果你[想要其中一种用于你自己的定制 3D 打印机制造](https://hackaday.com/2020/11/04/scratch-built-3d-printer-goes-big/)，请告诉他们。