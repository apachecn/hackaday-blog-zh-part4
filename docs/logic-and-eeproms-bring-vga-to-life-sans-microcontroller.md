# 逻辑和 EEPROMs 赋予 VGA 生命，无需微控制器

> 原文：<https://hackaday.com/2019/07/01/logic-and-eeproms-bring-vga-to-life-sans-microcontroller/>

不管出于什么原因，视频图形阵列标准似乎吸引了很多硬件黑客。他们中的大多数都倾向于欺骗微控制器来产生将图像发送到 VGA 显示器所需的信号。我们喜欢这些黑客，但这一个采取了不同的策略—[一个无微控制器的 VGA 显示器](https://www.reddit.com/r/electronics/comments/bz2xak/i_just_made_a_vga_signal_out_of_basic_logic_ics),它只使用简单的逻辑芯片和 EEPROMs。

当我们第一次发现这个项目时，[PH4Nz]还没有分享他的原理图和代码，但自从[在 GitHub](https://github.com/PHANzgz/VGAcontroller_v1) 上发布了一切。不过，他最初的描述足以吊起我们的胃口。他从一个 27.175 MHz 时钟开始，用 74HCT163 将其除以 4，其效果是将一个 EEPROMs 中存储的 160×240 像素图像扩展到 640×480。两个 8 位计数器跟踪水平和垂直位置，而另一个 EEPROM 负责产生 Hsync 和 Vsync 信号。这一切都很粗糙，但它的工作。[PH4Nz]告诉我们，整件事是在支持一个更大的项目:一台由逻辑芯片制成的 8 位计算机。我们也期待着看那部电影。

当然，这不是我们看到的第一个无微控制器 VGA 项目。这里的[是一个类似的也是基于 EEPROMs 的](https://hackaday.com/2017/03/07/vga-without-a-microcontroller/)，还有一个带 TTL 逻辑芯片的。我们仍然喜欢微控制器上的 [VGA，比如 ESP32](https://hackaday.com/2019/02/05/back-to-video-basics-with-an-esp32-vga-display/)；毕竟黑的方式不止一种。

感谢[John U]的提示。