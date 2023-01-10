# 在体二极管的帮助下废弃 EPROM

> 原文：<https://hackaday.com/2022/08/26/dead-eeprom-dumped-with-help-of-body-diodes/>

[杰森·P]，显然是老的可靠的激光打印技术的享受者，[把饮料](https://twitter.com/compu_85/status/1562044219874852864) ( [尼特](https://nitter.net/compu_85/status/1562044219874852864))洒到了他的松下·KX-P 5400 侧写器上。清理之后，一切正常——除了 PSU 的 5 V 在事故中变成了 6.5 V，带有 LocalTalk 接口固件的 EPROM 死了，VCC 和 GND 之间的连接似乎在芯片内部中断了。可以理解的是，[杰森]在推特上承认了自己的错误，并不好意思地向[询问 EPROM 转储。](https://twitter.com/compu_85/status/1562044267421483008)

相反，[【Manawyrm】想知道](https://twitter.com/Manawyrm/status/1563144774047367170)——该芯片会不会有从 GND 到 IO 引脚的防 ESD 体二极管？二极管模式万用表检查确认，是的！是时候进行一次奇怪的尝试来恢复固件了。[Manawyrm]建议[Jason]将除一个以外的所有输出引脚连接到 5 V，通过内部 VCC 连接的体二极管为 EPROM 供电——一次读取一位内容，然后将八个转储合并成一个图像。

在准备了 TL866 设置、一个小时的工作和一些 PHP 脚本之后，操作成功了。显然，在某些情况下，死的 ROM 芯片可能仍然会告诉他们的故事！不太清楚这里发生了什么。连接线看起来很好，所以谁知道连接是在哪里中断的-但我们不能否认恢复操作的成功！需要一本关于转储没有死的 EPROMs 的入门书吗？给你。

> 这是一个在过压或反向功率事件后从损坏的/有缺陷的 EEPROM 恢复数据的妙招:
> 
> 误用内部 ESD 保护二极管，通过数据引脚向芯片提供电压。然后用不同的位进行多次转储。[https://t.co/WHUiiaJdgf](https://t.co/WHUiiaJdgf)
> 
> —Manawyrm(@ Manawyrm)[2022 年 8 月 26 日](https://twitter.com/Manawyrm/status/1563178483165016065?ref_src=twsrc%5Etfw)