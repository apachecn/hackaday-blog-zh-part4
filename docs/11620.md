# 从未有过的无线 PS/2 键盘

> 原文：<https://hackaday.com/2021/10/16/the-wireless-ps-2-keyboard-that-never-was/>

PS/2 风格的端口曾经像今天的 USB 连接器一样在 PC 上无处不在，我们中的许多人都收集了大量带有 6 针迷你 DIN 插头的键盘和鼠标。今天它们已经不那么常见了，但是当你需要一个的时候，你就需要一个，所以如果你的 PS/2 键盘储备已经减少到没有了，你可能会想看看[推出你自己的 PS/2 远程键盘加密狗](https://remysharp.com/2021/04/14/building-a-ps2-remote-keyboard)。

关于[雷米·夏普]的背景故事始于他收购了一台 neptUNO，这是一台 160FPGA 改装计算机，它可以让你访问几乎所有过去的 Z80 和 6502 计算机。虽然这个盒子支持 USB 键盘，但[Remy]很难找到一个可用的。于是，一台 Wemos D1 迷你出来了，它被连接到一根 PS/2 电缆上。微控制器由 PS/2 端口供电，在启动时连接到 WiFi 网络，并启动 WebSocket 服务器。它还提供了一个 HTML 页面，让他可以连接任何设备，并向 neptUNO 发送按键。他还在加密狗上添加了几个硬件按钮，以便直接访问 neptUNO 上的菜单。下面的视频展示了它的作用。

也许不出所料，[Remy]说他从[Ben Eater]出色的 PS/2 深潜中获得了灵感。[我们认为他在这里第一次看到了这一点](https://hackaday.com/2021/03/11/decoding-the-ps-2-keyboard-protocol-using-good-old-fashioned-hardware/)，但无论如何，这是一个关于键盘如何工作的有价值的参考。

 [https://www.youtube.com/embed/s0uEqRh1oLU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/s0uEqRh1oLU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢【不规则棚】的提示。