# DC 终于有了自己的 PCB 地铁图

> 原文：<https://hackaday.com/2022/07/19/washington-dc-finally-gets-its-own-pcb-metro-map/>

曾几何时，就在不久前，想自己定制 PCB 的人会发现自己在市场上需要一桶酸和一台二手激光打印机。如今，你所要做的就是在你选择的 EDA 程序中点击几个按钮，然后将文件发送出去进行制作。这很简单，便宜，而且没有人会被化学烧伤。

这显然对电子爱好产生了变革性的影响——当你可以像艺术家使用画笔一样在 PCB 上放置轨迹时，你得到像[洛根·阿科马]的*DC 晶体管*T3 这样的项目只是时间问题。这种开源板使用精心排列的 RGB LEDs 来重建华盛顿大都会区交通管理局(WMATA)的地铁地图，由于 ESP8266 连接到他们的 API，可以实时显示火车的位置。

[![](img/3475fe5b917356cb0dc7118827e743ac.png)](https://hackaday.com/wp-content/uploads/2022/07/dctransistor_detail.gif) 如果你在这里有一种似曾相识的感觉，那不仅仅是在你的头脑中。我们已经看到了为其他主要大都市地区创建的类似地图，[洛根]当然不是想把这个想法归功于自己。事实上，他有点惊讶地发现，从来没有人为 DC 地区做过——所以他决定自己接受挑战。他认为这将是磨练他的 PCB 设计技能的好方法，并使他更加适应嵌入式开发。我们会说，最终结果证明了他的理论是正确的，并使另一个城市可以夸耀其物联网制图。

想在自己的墙上挂一个*DC 晶体管*？[Logan]说他将很快把电路板设计文件和原理图[放入该项目的 GitHub 库](https://github.com/LArkema/dctransistor-project)，他还计划在不久的将来出售预制电路板。

早在 2020 年我们就报道过这张[伦敦“地铁”地图，一年后](https://hackaday.com/2020/07/05/live-map-of-london-tube-created-in-pcb-and-lights/)[东京、新加坡和旧金山湾区](https://hackaday.com/2021/09/19/pcb-metro-maps-are-a-gorgeous-labor-of-love/)的类似展示对细节的关注给我们留下了深刻印象。也许是时候用 led 来描绘你自己的家乡了？