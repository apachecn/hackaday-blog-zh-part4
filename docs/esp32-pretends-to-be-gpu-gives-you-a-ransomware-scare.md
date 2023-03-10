# ESP32 冒充 GPU 让你害怕勒索软件

> 原文：<https://hackaday.com/2021/12/30/esp32-pretends-to-be-gpu-gives-you-a-ransomware-scare/>

有时一个硬件遇到一个恶作剧的想法，有趣的 Hackaday 文章就是这样诞生的。[AnotherMaker] [向我们展示了一些无害的娱乐活动](https://youtu.be/4qPo37wAf2s),代价是你生活中的一名 IT 爱好者——编写一个带 VGA 输出的 ESP32 驱动的 devboard，在与之相连的显示器上显示一个令人恐惧的“所有文件都加密了”的屏幕。8 位荣耀中的 ASCII 文本有助于推销这个恶作剧，使它看起来完全像它声称的 BIOS 劫持恶意软件；类似于过去熟练的黑客在 x86 汇编中使用的 ui。devboard 集成到 PCI 卡背板中是一个亮点，这是一种将它无缝集成到 PC 机箱中的方式，使它看起来与旧显卡没有什么特别的不同。在这样的配置中，我们不怀疑这对于某种类型的 IT 部门工作人员来说是个难题。

如果你已经有了这个恶作剧的目标，你很幸运，因为[AnotherMaker] [也分享了他的源代码](https://github.com/mudmin/AnotherMaker/tree/master/diabolocal-it-prank)，你所需要的只是一个设置了 VGA 端口的 ESP32。你可以得到相同的开发板，或者如果你有时间或金钱预算，你甚至可以用 ESP32 分线点和电阻将它们焊接在一起，因为[lily go 开发板的原理图是公开的。](https://github.com/LilyGO/FabGL/blob/master/Schematic/vga32_v1.4.pdf)并不是所有的 devboards 都有这么有趣的应用程序，但看到有人想到一个应用程序总是很有趣——这是一个完美的恶作剧，需要一个非常特殊的 devboard。

想知道如何从 ESP32 输出 VGA 吗？我们在过去已经报道过这一点——比如由[bitluni]完成的这个研发项目,然后他通过[一次连接*六个*显示器](https://hackaday.com/2021/08/18/running-six-vga-projectors-from-a-single-esp32/)来继续并扩展它。如果你已经将你的 ESP32 连接到 VGA 端口，并运行了一些测试草图，[一个 UI 库](https://hackaday.com/2019/07/08/esp32-gets-advance-windowed-apps-using-this-vga-gui-library/)将帮助你立即将你的想法升级为一个现成的项目。

 [https://www.youtube.com/embed/4qPo37wAf2s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4qPo37wAf2s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

