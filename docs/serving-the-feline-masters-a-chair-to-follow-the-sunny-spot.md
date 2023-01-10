# 为猫主人服务:跟随阳光的椅子

> 原文：<https://hackaday.com/2021/01/17/serving-the-feline-masters-a-chair-to-follow-the-sunny-spot/>

特里·普拉切特曾写道:“在古代，猫被当作神来崇拜；他们没有忘记这一点”。[乔纳森]的猫显然没有忘记，每当她最喜欢的椅子需要移动以保持在阳光的地方时，它都会大声告知。无论如何，他都在寻找一个有趣的黑客，所以他决定屈服于女王陛下的要求，并自动完成任务。

[Jonathan]首先考虑将椅子本身机动化，但决定保持简单，只需用一个连接到马达的卷轴将椅子拖过房间。绳索线轴连接到安装在沙拉碗底座上的小型齿轮传动 DC 电机，并通过电机驱动器连接到 ESP8266。8266 运行 NodeMCU 和一个 web 服务器，该服务器通过 RESTful API 接受简单的电机命令。这种设置无法在一天结束时将椅子重置到其起始位置，但这是为简单性付出的小小代价。电机有点动力不足，但它只需要一次移动椅子一小段距离，所以[乔纳森]移除了椅子的靠背以减轻重量，并提高了电机电压。

决定何时移动椅子以及移动多远是挑战的第二部分。[Jonathan]考虑了一个简单的时间查找表，但是马达的运动不够一致。最终的解决方案是一组三个 BH1750 数字环境光传感器来提供反馈。椅子上的一对传感器通过将光线水平与安装在窗户上的参考传感器进行比较，来确定其相对于阳光照射点的位置。这些光传感器也连接到 NodeMCUs，并在必要时向卷绕装置发送移动命令。

不幸的是，黑客似乎是徒劳的，因为最终用户被马达的噪音吓跑了。然而，这仍然帮助[乔纳森]挠了挠他的黑客之痒，对我们来说幸运的是，他记录了这次冒险，并分享了所有的代码。

这是我们报道的第一张猫椅，但是我们已经看到一些黑客[喂它们](https://hackaday.com/2019/12/30/cat-diner-now-under-new-management/)或者[把它们赶走](https://hackaday.com/2020/10/09/tiny-trash-can-repels-trash-pandas-medium-sized-cats/)。

 [https://www.youtube.com/embed/Gj3qQ3IJx0A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Gj3qQ3IJx0A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

