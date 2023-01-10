# 复古未来谢妮科尔维尔仪表板

> 原文：<https://hackaday.com/2022/02/18/retro-future-nixie-corvair-instrument-panel/>

我们今天所知的未来与 60 年代和 70 年代所设想的大不相同。首先，它的谢妮管太少了。一名监督人员[nixiebunny]想用他的 Nixie tube 仪表盘来解决[的问题。](https://www.reddit.com/r/nixie/comments/smv9b5/nixie_tube_instrument_panel_in_my_corvair/)

所有必要的信息都在那里:发动机温度，转速表，速度，电池电压，甚至里程表。你可能已经注意到这里没有时钟。[nixiebunny]给出的理由是，他总是戴着他的谢妮手表，所以在他的车里放一个时钟似乎是多余的。面板上还有一个间隙，可以显示油压。众所周知，Corvairs 会将皮带扔在机油发送器旁边，因此任何附加的传感器都需要经过精心设计和深思熟虑。一个十几岁的孩子从发动机舱接收发动机遥测数据(没有 OBDII 端口可以连接——通用汽车直到 80 年代才推出第一个 OBD 端口)。数据转换为 SPI 数据，通过 CAT5 电缆发送到 74HC595 移位寄存器链。细节有点稀疏，但我们可以看到一个定制的 PCB，以适应仪表板上的孔的形状，并在其上丝网印刷不同的数码管足迹。

我们喜欢在意想不到的地方看到谢妮管。像[这个 POV 谢妮钟](https://hackaday.com/2021/05/07/this-pov-clock-combines-a-nixie-with-a-pendulum/)或者这个[谢妮机器人雕塑](https://hackaday.com/2021/08/22/artful-nixie-bot-sculpture-sees-thinks-and-talks/)。