# 超级链接和超功能文本 CAD

> 原文：<https://hackaday.com/2020/09/30/hyper-links-and-hyperfunctional-text-cad/>

关于 OpenSCAD，双方都有强烈的意见。轻量级程序占用兆字节的空间，而不是千兆字节，所以许多人都有一个副本，即使他们从来没有写过一个形状。有些人崇拜纯文本建模语言，有些人厌恶最小函数列表。[Johnathon 'Zalo' Selstad]欣赏这个想法，但希望看到更强大的东西，他希望在您的浏览器中看到它。他的项目 CascadeStudio 有一个 [GitHub repo](https://github.com/zalo/CascadeStudio/) 和[一个实时链接，所以你可以马上在一个新窗口中开始修补](https://zalo.github.io/CascadeStudio/)。

我们将假设任何读到这里的人都熟悉这种类型的建模。

在第一次击键时，很明显 CascadeStudio 不同于 OpenSCAD。首先，工具提示显示格式有点不同。OpenSCAD 中的圆锥体使用 cylinder()函数，而 CascadeStudio 坚持认为 cylinder()在顶部和底部具有相同的直径，但是 [Cone()](https://zalo.github.io/CascadeStudio/?code=lVNNb9swDL37V7C5rBkURGmawz56adJhAwasaDp0a5GDJtGxEEUyJLlL%2Fv0o2flAVmCrYVtPJN8jRdPDITygkW6NEB1MRZBCIcxjo7Q7A4DP6BEEPSGFNAHLxkDZWBm1s%2BF9MRwC3HthgxERz%2FsM7lzs0FwKk8F3S7EJzHRZkp6V2fzFRvQBs9J5Pytdu01m1hWFJTTdGm0V%2BoydzbZ73MTxLKFbZ7bLPflbWQaMyX6zib5RR%2BWoYws%2BO%2FOc4a2u8%2FrVlZmXZT5pYzDeqCWGnLUSayp6t88hc6O7mq6bGNuzTSuUq1%2Bp%2FqIgPlTO4J1QuglwtSP0WkOPwZgDg4v0uuT9Dy0j5FNDuq52LZgkb3LKrhGPyfnSte%2FUIXHKwBnQyfFE5WdS6b7UE2cjxhcM3nH2L5UTmR%2FHMiTyCpniMDRUANA9SeSjCWnbweBpn40d6j%2FAx8Wp3GDEW8XLpNhNS%2B%2BBOvtxTAMt5Eoose39XQVnE%2F72YtFN2mgnkgJPezUmz%2F9xXyAPXsVOEzdz9k2E0vkldZ%2F%2B07oJFeh17TzNNjgPTg4UltrSLlSixgDaUlyQaHHeGmgrlIJY4TphWuG386tQC4lnxR8%3D&gui=q1ZKzs8tyM9LzSvxS8xNVbJSSk4sTk5MSQ3LTC1X0lHyTS3OCEotVrIy0DOE84IS89KBSqMN9AwMdYxidZScE5MzUu2VrEqKSlN1lIISUzJLgVqMDWBsmAYjAx0Tg9haAA%3D%3D) 逐渐变细。你可能还会注意到 CascadeStudio 的大写字母。这种程度的微小差异意味着任何熟悉其中一个的人可能会遇到另一个的减速，但不会遇到障碍。

在我们看来，CascadeStudio 最大的好处是你可以给某人发送一个 URL，他们将获得一个全功能的副本。你不能像谷歌文档一样同时编辑，但可以想象在二维码或 RFID 标签中存储 3D 模型，可能没有 URL 缩写。每次按 F5 刷新渲染模型时，URL 都会更新，因此可以使用浏览器书签创建带日期的保存点。如果您喜欢下载文件，可以保存和加载 JSON 文件，并且可以为您的打印机导出 STEP、STL 和 OBJ 文件。

请告诉我们您对 CascadeStudio 的看法，以及这是否改变了您对基于文本的建模的想法。我们已经看到这种参数化的工具处理日常任务，如[容器盒](https://hackaday.com/2019/03/11/openscad-gives-you-parametric-boxes/)到[高安全性钥匙](https://hackaday.com/2019/09/24/copying-high-security-keys-with-openscad-and-light/)。