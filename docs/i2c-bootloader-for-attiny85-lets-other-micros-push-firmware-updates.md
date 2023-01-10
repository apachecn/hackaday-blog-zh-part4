# ATtiny85 的 I2C 引导程序允许其他微处理器推送固件更新

> 原文：<https://hackaday.com/2018/10/20/i2c-bootloader-for-attiny85-lets-other-micros-push-firmware-updates/>

有几种不同的方法可以将固件安装到 AVR 的 ATtiny85 微控制器上，包括允许固件更新而无需将芯片插入编程器的引导加载程序。然而，[casanovg]对这些并不满意，所以他给我们发了一个提示，让我们知道他写了一个名为*帝汶人*的 ATtiny85 的 I2C 引导程序。它考虑了器件的一些细节，例如它缺少引导加载程序通常驻留的受保护内存区域，并且它没有本机 I2C 接口，只有 USI(通用串行接口)。他刚刚发布了 ATtiny85 的第一个功能版本，但没有理由不让它也适用于 ATtiny45 和 ATtiny25。

Timonel 是为有更强大的微控制器或微处理器运行的系统而设计的(例如 ESP8266、Arduino，甚至是像 Raspberry Pi 这样的板。)在 ATtinys 位于 I2C 总线上执行外设功能(如运行传感器)的设计中， *Timonel* 允许这些外设 MCU 的固件直接从 I2C 总线主控器更新。下面嵌入的是[casanovg]发送简单串行命令的视频演示，展示了 I2C 上空 AVR ATtiny85 的成功固件更新。

 [https://www.youtube.com/embed/-7GOMToGvzI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-7GOMToGvzI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



ATtiny85 往往会在许多小型项目中出现，比如这个[微型函数发生器](https://hackaday.com/2018/03/02/tiny-function-generator-on-the-attiny85-complete-with-oled/)和[名片俄罗斯方块](https://hackaday.com/2018/05/20/tiny-sideways-tetris-on-a-business-card/)。