# 开源 LXI 工具使我们摆脱了供应商膨胀

> 原文：<https://hackaday.com/2022/02/18/open-source-lxi-tools-free-us-from-vendor-bloat/>

LXI 或仪器仪表局域网扩展是连接支持以太网的电子仪器仪表的现代控制标准。它取代了旧的 GPIB 标准，提供了更好的性能和更低的实施成本。这是好事。[Martin Lund]创建了[开源 lxi-tools 项目](https://github.com/lxi-tools/lxi-tools),它使我们能够脱离通常将 lxi 与您的工作台设备对话所需的臃肿的供应商工具。这是该工具早期版本的部分重写，现在拥有一些相当不错的功能，如用于工具发现的 mDNS、对屏幕抓取的支持以及基于 LUA 的脚本后端。( [API 链接](https://github.com/lxi-tools/lxi-tools/blob/master/doc/lua-api.txt)

[SCPI 或可编程仪器的标准命令](https://en.wikipedia.org/wiki/Standard_Commands_for_Programmable_Instruments)是许多仪器使用的基于文本的语言，允许对仪器进行控制和查询。需要说明的是，SCPI 一点也不新鲜，有 GPIB 或 RS232 连接器的老式仪器仍然可以使用 SCPI。lxi-tools 不适合这些。一些工具对命令的格式也很挑剔，尤其是当它们有问题时，所以交互调试命令的能力是非常理想的。很有可能在测试脚本中没有很好地使用 SCPI 命令，最终导致测试执行起来比需要的时间长得多。lxi-tools 也有一个基准测试工具，可以帮助您深入了解并找出所有时间的去向，并做出适当的调整。

我们在 Hackaday 上没有看到太多关于 LXI 的内容，但是我们确实介绍了使用 [PyVISA 来处理 python 中的 SCPI-over-GPIB](https://hackaday.com/2016/11/16/how-to-control-your-instruments-from-a-computer-its-easier-than-you-think/) 。如果你有一个带 GPIB 的旧乐器，并且你不想卖内脏来买 USB 适配器，[这里有一个你可以自己做的](https://hackaday.com/2014/05/09/gpib-to-usb-with-a-python-api/)。