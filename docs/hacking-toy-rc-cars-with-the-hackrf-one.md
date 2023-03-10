# 用 HackRF 一号黑客玩具遥控车

> 原文：<https://hackaday.com/2022/04/30/hacking-toy-rc-cars-with-the-hackrf-one/>

对于许多自称为黑客社区成员的人来说，最初的故事通常是从小时候拆开东西开始的，只是为了看看它们是如何工作的。对拉多斯拉夫来说，这种趋势似乎没有减缓，他继续拆卸玩具。尽管因为这是他女儿的无线电遥控小汽车，他坚持非破坏性拆卸。结果呢？他能够通过 HackRF One SDR 收发器用他的笔记本电脑[控制汽车，如休息时间下方的视频所示。](https://xakcop.com/post/re-2.4ghz/)

[Radoslav]对嵌入式设备、物联网小工具以及可能更多的逆向工程并不陌生。所以他从公开可用的关于正在使用的无线电控制接口的信息开始。许多在美国销售的电子设备必须通过 FCC(联邦通信委员会)的认证，并在显著位置显示其 ID 号，这个玩具也不例外。FCC 数据库给了[Radoslav]足够的信息，让他知道通信协议是用 GFSK 调制的，这是一种频移键控。

他启动了他最喜欢的无线电[信号分析工具](https://github.com/miek/inspectrum)，开始研究协议本身。在这个过程中，他发现汽车和控制器之间的通信是双向的，但也很容易实现。结果是他可以带着他的笔记本电脑开着车到处跑——这绝对是一个很酷的技术，但对于这个人来说，旅程肯定是目标，而不是目的地。

如果对遥控汽车的黑客攻击真的让你的车轮转动起来，你可能会喜欢这辆可以在天花板上驾驶*的小[遥控汽车。](https://hackaday.com/2021/09/04/fan-lets-rc-car-drive-on-the-ceiling/)*或者，如果你觉得有点饿，试试如何使用 [HackRF 在你当地的餐馆订到一张桌子](https://hackaday.com/2019/06/04/your-table-is-ready-courtesy-of-hackrf/)。

 [https://www.youtube.com/embed/mqSv-Nycy_4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mqSv-Nycy_4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

