# 从 CircuitPython 入侵 Hackaday.io

> 原文：<https://hackaday.com/2019/01/18/hacking-hackaday-io-from-circuitpython/>

如果你曾经参与过社交媒体，你会很熟悉当你的帖子、推文或项目获得赞时的那种小兴奋。但是，如果登录感觉开销太大，无法获得多巴胺奖励，那么[pt ' s][circuit python hack aday portal](https://hackaday.io/project/163309-circuitpython-hackaday-portal)可能正是你正在寻找的。这个项目创建了一个独立的计数器来显示 hackaday.io 上的一个项目收到的“skulls”(又名 likes)的数量，当然，它目前正在统计自己的数量。

代码运行在 SAMD51 (Cortex M4)微控制器上，并在 240×320 TFT 显示器上显示头骨。对于 WiFi 连接，该项目使用一个通过通常的 AT 命令集控制的 ESP-32。这种交互的所有血淋淋的细节都被 CircuitPython 库抽象掉了，这很好，因为您真的不想为每个项目都编写这样的代码。该程序访问 hackaday.io API 来检索项目的 skulls 数量，但是可以很容易地修改以与任何返回 JSON 结果的服务接口。

最近我们看到了很多 CircuitPython 代码。以防你不熟悉，CircuitPython 是 Adafruit 的 MicroPython 版本，这是一种针对嵌入式处理器的 python 语言。虽然这听起来像是纯粹为了让守旧派 embedded-C 程序员发牢骚而炮制的东西，但它实际上对于嵌入式原型开发和开发来说非常强大和方便。在最新廉价微控制器的速度和快速增长的一组库的推动下，它为使用集成外设和常见的黑客友好部件提供了可靠的替代方案。如果你想开始，这里有很多例子，我们在 hackaday.io 上维护了我们自己的 CircuitPython 项目列表,你可以查看。

休息之后你可以看到一段视频。这不是一个实时流，所以你不会看到你的喜欢出现在显示器上，但请放心，[pt]会！

 [https://www.youtube.com/embed/25GxRfRNCCI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/25GxRfRNCCI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们以前看过[pt]的作品。包括——你知道——写我们的第一篇文章。