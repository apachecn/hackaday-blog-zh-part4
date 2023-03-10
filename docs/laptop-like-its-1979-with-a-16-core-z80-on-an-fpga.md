# 就像 1979 年的笔记本电脑，FPGA 上有一个 16 核 Z80

> 原文：<https://hackaday.com/2019/12/10/laptop-like-its-1979-with-a-16-core-z80-on-an-fpga/>

当生活递给你一个贵得离谱、功能强大的 FPGA 开发板时，你的第一反应可能不是[用它来构建一个 16 核 Z80 笔记本电脑](http://www.chrisfenton.com/the-zedripper-part-1/)。如果不是，也许你应该检查你的优先事项，因为这就是[克里斯·芬顿]所做的，其结果是非常不切实际的“ZedRipper”

我们的第一印象是，我们已经开始在一个更好的实验室周围闲逛，因为[Chris]在一次实验室清洗后得到了这个 6000 美元的 FPGA 板；我们得到的最好的东西是一些旧的 Cat-5 电缆和一些电源板。Stratix FPGA 构成了设计的核心，周围是一些用于 10.1 英寸 VGA 显示器和键盘的分线板，键盘是从旧的 PS/2 中抢救出来的。FPGA 中运行的 16 个 Z80 内核通过一个环形拓扑网络连接起来，[Chris]称之为“Z 环”。Z80 核心中的一个，即服务器核心，运行 CP/M 2.2 和一个名为 CP/NET 的文件服务器，而其他 15 台机器是运行 CP/NOS 的客户端。一个简单的窗口管理器可以同时显示服务器和任意三个客户端的 80 x 25 字符终端会话，包括 LiPo 电池组在内的所有内容都可以放入激光切割的胶合板箱中。这是复古，这是现代，这是矫枉过正，我们绝对喜欢它。

阅读[Chris]的构建日志让我们有心情拿出[我们的 2019 年超级大会徽章](https://hackaday.com/2019/11/04/gigantic-fpga-in-a-game-boy-form-factor-2019-supercon-badge-is-a-hardware-siren-song/)，并尝试打造我们自己的 Z80。如果你决定黑掉 FPGA-est 的会议徽章，你可能想看看[[Sprite _ TM]对此有何评论](https://www.youtube.com/watch?v=X39nnPWmkvA)。毕竟是他设计的。你肯定想看看[我们在 super co](https://hackaday.com/2019/11/29/a-fantastic-frontier-of-fpga-flexibility-found-in-the-2019-supercon-badge/)看到的一些令人敬畏的徽章破解。

感谢[yNos]的提示。