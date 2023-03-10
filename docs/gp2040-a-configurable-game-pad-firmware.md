# GP2040:一个可配置的游戏手柄固件

> 原文：<https://hackaday.com/2022/09/04/gp2040-a-configurable-game-pad-firmware/>

[feralAI]和其他 GitHub 贡献者为您带来了观看乐趣 [GP2040:一个基于 RP2040 硬件的开源游戏手柄固件](https://gp2040.info/)。双核 RP2040 是一个用于游戏输入的良好平台，因为无论控制器可能正在执行任何其他任务，都有大量 CPU 负载来获得不到 1 毫秒的 USB 轮询时间。目前固件支持 PC，Android，RPi，任天堂 Switch，PS3，PS4(传统模式)，和甜蜜的[先生基于 FPGA 的复古游戏平台](https://hackaday.com/2021/09/12/hey-mister-emulator-gimme-almost-any-classic-platform/)。

固件支持旧的 [DirectInput API](https://en.wikipedia.org/wiki/DirectInput) 和新的闪亮(但相当严格)的 XInput API(不，它不是同名的旧 X11 输入扩展)——以及常见的控制器功能，如 [SOCD](https://www.hitboxarcade.com/blogs/support/what-is-socd) 清洁，D-pad 映射，以及对额外干扰的 RGB 支持。甚至还有对那些微型有机发光二极管显示器(SSD1306 和 friends)的支持，尽管我们目前还想不出这样的用例。然而，配置尤其有趣，因为它是基于嵌入式 web 应用程序的。这是定义到实际硬件的管脚映射的地方，如果你愿意的话，还有所有的 RGB 闪烁。

但是你会问，不起眼的 RP2040(无论是 Pico 还是兼容的)如何提供网页呢？快速的答案来自微软和他们的远程网络驱动程序接口规范(RNDIS)的支持。RNDIS 通过 USB 实现了一个网络设备，幸运的是，其他操作系统已经赶上并实现了它。GP2040 固件利用 [TinyUSB](https://github.com/hathach/tinyusb) 来实现 RNDIS 协议， [lwIP](https://savannah.nongnu.org/projects/lwip/) 来实现轻量级网络堆栈(同时只占用相当少的 40k 闪存)，最后 [react-bootstrap](https://react-bootstrap.github.io/) 来编码实际的 web 逻辑。(现代开源库是不是很牛逼？)如果你觉得有必要使用源代码(不管你是不是叫 Luke)，这个项目可以在 [GP2040 GitHub](https://github.com/FeralAI/GP2040) 上找到。

如果你喜欢在游戏手柄上玩游戏，但又非常喜欢可靠的鼠标的响应能力，那么看看这款[简洁的混合控制器](https://hackaday.com/2020/12/15/mouse-controller-hybrid-aims-to-dominate-in-first-person-shooters/)就够了。但是如果这种到处都是 45 个按钮和控制杆的现代东西太多了，而且你渴望老式的控制器，[这可能更适合你的风格](https://hackaday.com/2022/06/15/odd-inputs-and-peculiar-peripherals-a-joystick-like-they-used-to-make/)。

感谢 [Hackaday Discord 服务器](https://discord.com/invite/NkbHrAW7NG)上的【DJBiohazard】提供的提示！