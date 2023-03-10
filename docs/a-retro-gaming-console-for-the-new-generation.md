# 新一代的复古游戏机

> 原文：<https://hackaday.com/2019/10/01/a-retro-gaming-console-for-the-new-generation/>

表面上看， [ESPboy 是一个开源的可黑客攻击的游戏引擎](https://hackaday.io/project/164830-espboy-games-iot-stem-for-education-fun)，作为 STEM 教育和游戏的物联网平台，但[ [罗马人](https://hackaday.io/ESPboy.edu)不可能受到除了不久前复古游戏机以外的任何东西的启发。对于任何从小玩电子鸡宠物或掌上电脑长大的人来说，这个项目将是一个重大的倒退。

这位圣彼得堡的微控制器爱好者利用 ESP8266 微控制器构建了一系列用于不同游戏模式的模块，包括 TFT 显示屏、GSM 电话、MP3 播放器、GPS 导航仪、FM 收音机和键盘模块。他计划建造更多的模块，包括 LoRa messenger 和热感相机，以真正扩展该系统的能力。

由于主板内置 WiFi，固件可以上传到设备，无需有线连接和编译器。该项目的性质使得该板与 Arduino IDE 和 Micropython 兼容，这使得破解该软件更加容易。

TP4056 电池充电模块为 LiPo 充电，但根据电池容量，充电电流(由控制器上的 R3 电阻设置)确实需要一些变化。MCP4725 I2C DAC 用于平滑驱动 LCD 的背光。为了延长电池寿命，电池控制器使用睡眠模式来定期唤醒以测量和发送数据，这允许它在没有外部电源的情况下延长电池寿命。还有晶体管驱动的蜂鸣器，在玩游戏时为用户提供一点额外的反馈，并配有一个可变电阻器来调节音量。

 [![espboy r3](img/54c785d7f3f69d3c57043650ea2b8f5e.png "espboy r3")](https://hackaday.com/2019/10/01/a-retro-gaming-console-for-the-new-generation/espboy-r3/)  [![espboy transistor buzzer](img/cf9beb829e424cd21b37321001d88c13.png "espboy transistor buzzer")](https://hackaday.com/2019/10/01/a-retro-gaming-console-for-the-new-generation/screen-shot-2019-09-30-at-9-50-09-am/) 

许多自由引脚沿外围延伸，用于连接其他模块，包括 GPIO 扩展引脚、传感器适配器、可寻址 led 连接器和致动器扩展插槽。对于任何有兴趣制作自己版本的 ESPboy 的人来说， [PCB 原理图可在线获取](https://easyeda.com/roman.sokolov/espboy-rev2-4)。

像 Arduboy 这样的项目已经表明，基于微控制器的小型游戏系统[既有趣又有教育意义](https://hackaday.com/2019/07/01/schools-in-session-with-arduboy-curriculum/)，所以我们很高兴看到更多这种类型的项目[在 2019 年 Hackaday 奖](https://hackaday.com/2019/09/19/pew-pew-in-the-palm-of-your-hand/)期间涌现出来。

 [https://www.youtube.com/embed/sHrSPXpTcYI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sHrSPXpTcYI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)