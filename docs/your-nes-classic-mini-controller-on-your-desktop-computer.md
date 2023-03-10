# 台式电脑上的 NES 经典迷你控制器

> 原文：<https://hackaday.com/2021/01/24/your-nes-classic-mini-controller-on-your-desktop-computer/>

NES 经典迷你是早期发布的经典复古游戏机迷你版本的更广泛趋势之一。每个人都想要一个，但数量有限，所以只有少数幸运儿获得了这个机会，在真正的任天堂硬件上通过*大金刚*或*马里奥兄弟*重温他们的童年。显然[ 阿尔伯特·冈萨雷斯是其中之一，因为他为迷你控制器生产了一个 USB 适配器[，使其可以用作 PC 外设](https://hackaday.io/project/176939-nes-mini-controller-usb-adapter-with-attiny85)。

在小原型板上，一端是任天堂连接器，另一端是 ATtiny85 微控制器和微型 USB 连接器。通过 V-USB 库的魔力，控制器的 I2C 接口被映射到 ATtiny 上的 USB，对后者来说就像一个普通的游戏手柄。人们认为，同样的界面很可能也适用于后来的 SNES 经典迷你控制器。出于好奇，所有的代码和其他资源[都可以在 GitHub 仓库](https://github.com/koopaconan/nesmini_usb_adapter)中找到，所以如果你足够幸运能买到 NES 经典 Mini，那么你也可以加入 PC 乐趣。

迷你游戏机很受欢迎，但并没有像预期的那样让我们的社区兴奋。我们的同事 Lewin Day tool 去年夏天研究了这一现象。