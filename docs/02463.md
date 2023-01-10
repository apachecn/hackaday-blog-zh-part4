# M0 皮层成为平台-游戏平台

> 原文：<https://hackaday.com/2019/03/20/cortex-m0-becomes-platform-game-platform/>

Arduino Uno 是一个非常受欢迎的微控制器平台。由于简单易懂，并且处理能力足够危险，它赢得了全世界的粉丝。最近，有人试图用更强大的东西来取代它。Arduino Zero 就是这样一款试图夺取桂冠的设备，[和【Nicola Wrachien】决定尝试在平台](https://hackaday.io/project/164367-40-fps-16-bpp-platform-game-on-a-cortex-m0-board)上开发游戏。

[Nicola]选择使用 uChip，这是将 Arduino Zero 重新组合成更小的外形。这与 160×128 TFT 显示屏和一些控制按钮结合在一起。uChip 模块与 TFT 一起安装在[Nicola]定制的 PCB 上，将一切联系在一起。

通过将 SPI 端口超频至 24 MHz，[Nicola]能够以超过每秒 50 帧的速度运行基本的 2D 平台。帧速率被限制在大约 40 fps，以保持流畅和稳定，结果令人印象深刻。游戏流畅且反应灵敏，每像素 16 位的屏幕看起来充满活力，提供了丰富的色彩。

我们喜欢看到游戏系统从原始的微控制器和显示器中切割出来。[Nicola]的工作表明，只要稍加修改，就可以获得显著的性能提升。对于同样令人印象深刻的 DIY 手持黑客，请查看 Arduboy 上的 Star Fox。休息后的视频。

 [https://www.youtube.com/embed/-dM5cK1SgUk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-dM5cK1SgUk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

