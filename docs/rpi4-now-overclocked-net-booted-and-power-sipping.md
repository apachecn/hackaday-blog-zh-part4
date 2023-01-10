# RPi4:现在超频，网络启动，功耗低

> 原文：<https://hackaday.com/2019/10/30/rpi4-now-overclocked-net-booted-and-power-sipping/>

树莓 Pi 4 发布已经有几个月了，用“不稳定”来形容这次发布是公平的。虽然在纸面上比 Pi 3 快得多，但它的过热倾向最终会降低 CPU 时钟，即使有过多的售后散热器和风扇。Raspberry Pi 的人一直在努力解决这些初期问题，他们现在已经发布了一系列更新，形式是一个新的引导加载器，让 Pi 4 实现它的承诺。(**更新:**这里是[下载页面](https://www.raspberrypi.org/downloads/)和[发布说明](https://github.com/raspberrypi/rpi-eeprom/blob/master/firmware/release-notes.md)

更新的实质是 USB 集线器实现了低功耗模式。原来，SoC 上的主要热源不是 CPU，而是 USB。固定 USB 功耗意味着您可以以库存速度运行处理器，现在甚至可以超频。

还有一个更新 Pi bootloader 的新工具， [rpi-eeprom，](https://github.com/raspberrypi/rpi-eeprom)允许 Pi 4 拥有者自动更新。最大的变化是现在可以通过网络或一个连接的 USB 设备启动 Pi 4，如果你要永久安装 Pi 的话[必须这么做](https://hackaday.com/2018/10/08/hack-my-house-running-raspberry-pi-without-an-sd-card/)。有一些修复导致了某些 HATs 的问题，其中 Pi 4 的 3.3 V 线在重新启动时被循环。

对于像树莓派这样复杂的设备，它可能会出现一些初期问题也就不足为奇了。我们已经介绍过一些周边的[，例如 USB-C 电源](https://hackaday.com/2019/07/16/exploring-the-raspberry-pi-4-usb-c-issue-in-depth/)。还有过热的。Pi 人员始终如一地提供来自官方和社区的支持，我们很高兴看到他们在这种情况下也能提供支持。