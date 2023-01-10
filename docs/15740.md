# DietPi 版支持 Rockchip RK3588 SoC

> 原文：<https://hackaday.com/2022/12/27/dietpi-releases-8-12-with-support-for-the-rockchip-rk3588-soc/>

这个月 DietPi 发布了面向 SBC 的 Linux 发行版的 8.12 版本。最值得注意的是增加了对纳米皮 R6S 和[Radxa ROCK 5B](https://wiki.radxa.com/Rock5/hardware/5b)SBC 的支持。ROCK 5B 采用新的旗舰 Rockchip RK3588 SoC，配有四核 Cortex-A76 和四核 Cortex-A55。与 Debian、Raspberry Pi OS 和 Armbian 等选项相比， [DietPi](https://dietpi.com/) 作为一款不仅适用于高端单板机，也适用于低端单板机的操作系统，令人感兴趣的是它非常注重成为[优化程度最高的](https://dietpi.com/stats.html)。这意味着更小的二进制文件大小、更低的 RAM 使用量和更优化的性能。

DietPi [的设置体验](https://dietpi.com/docs/)和前面提到的选项一样简单，除了从 bat 开始你就可以得到更多的调整选项。虽然开箱即用的体验和点击确定所提供的默认设置可能已经让大多数用户非常满意——像[可选图形界面](https://dietpi.com/docs/getting_started/)这样的东西很容易添加——但有事业心的用户可以[调整关于硬件、文件系统等的细节](https://dietpi.com/docs/dietpi_tools/#dietpi-configuration)。

当我们在 Raspberry Pi Zero 上设置 DietPi 时，它肯定比当前基于 Debian Bullseye 的 Raspberry Pi 操作系统更轻量级。尽管 DietPi 也是基于 Debian 的，但它留出了更多的内存和存储空间，这对于在像 Raspberry Pi Zero 这样的有限平台上运行来说无疑是一个福音。不管在公共场合这样说是否礼貌，DietPi 肯定会说现在很多标准的 SBC 图像都很矮胖。