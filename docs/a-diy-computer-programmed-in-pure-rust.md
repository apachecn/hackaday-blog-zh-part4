# 用纯 Rust 编程的 DIY 逆向计算机

> 原文：<https://hackaday.com/2019/10/21/a-diy-computer-programmed-in-pure-rust/>

你能生成 VGA 并使用 Rust 中的 Cortex-M4 操作 PS/2 键盘吗？这正是[j pster]想用 [Monotron](https://hackaday.io/project/160791-monotron) 找到的答案，这是一台用纯 Rust 编程的 80 年代风格的家用电脑。

为了在没有工作的操作系统的情况下运行嵌入式 Rust，一些工具是必要的:用于生成机器代码的 LLVM 后端，用于指定内存大小和其他配置的目标文件，以及在运行操作系统时作为编译器替代品的预编译 libcore。Rust 取代了运行在板支持包(BSP)和硬件抽象层(HAL)以及指定硬件并允许代码跨不同芯片移植的外围设备访问箱(PACs)之上的 C。

[实现](https://github.com/thejpster/monotron)生成 60 Hz 的 800 x 600 VGA 视频信号，在 48 字符×36 行显示器上显示文本，使用颜色查找显示彩色图形(存储在闪存中)，并运行所有数据占用不到 24 KiB 的应用程序。Monotron 还通过 PWM 生成 8 位音频，并配备一个合成器，该合成器使用三通道波表，允许它用方波、正弦波、锯齿波发出声音，并创建白噪声。

到目前为止，Monotron 已经能够与 Atari 操纵杆、PS/2 键盘一起工作，并具有 VGA、MIDI、SD 卡和音频输出。Monotron 的下一步:编写编程语言(暂定名为 Monotronian)，添加对 Sega Megadrive pads 的支持，显示精灵，以及许多更令人兴奋的开发。

 [https://www.youtube.com/embed/PXaSUiGgyEw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PXaSUiGgyEw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)