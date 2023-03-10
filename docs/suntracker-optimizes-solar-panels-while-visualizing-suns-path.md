# Suntracker 优化太阳能电池板，同时可视化太阳的路径

> 原文：<https://hackaday.com/2019/08/18/suntracker-optimizes-solar-panels-while-visualizing-suns-path/>

如果你有太阳能电池板，你会想尽可能多地吸收阳光，让你的钱物有所值。如果你没有足够的空间来放置大量的面板，下一个最好的办法就是重新放置面板来捕捉最多的光线。为了参加 Hackaday 奖，[Frank]建造了一个华丽的太阳能追踪器原型来验证他的理论，并作为一个学习平台。

太阳能跟踪器的目的是——你猜对了——跟踪太阳的位置，以确定太阳能电池板和其他寻找太阳的有效载荷的最佳位置。在最新的版本中，[弗兰克]的追踪器跟随太阳的方位角，也就是它的水平运动。[![](img/9fd6a271cdf8975f9035f766c1d9bbbd.png)](https://hackaday.com/wp-content/uploads/2019/08/solar-tracker.gif)

太阳的路径由 32 个红色/绿色发光二极管组成的圆环表示。根据一个实时时钟和存储在 SD 卡上的一组预先确定的太阳位置,它像一个绿色 LED 一样绕着圆环移动。

两个红色 LED 显示日出和日落的方位角，第三个 LED 显示用磁力计检测到的北方，并根据当地的磁偏角进行调整。在圆环的中心，一个步进电机驱动一个总是指向太阳 LED 的箭头。随着追踪器的移动，所有的发光二极管围绕着圆环移动，以跟踪它们的目标。

虽然它已经闪耀，我们认为这个正在进行的项目有一个光明的未来。休息之后，请务必观看演示视频。

 [https://www.youtube.com/embed/e8dpviy-tlI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e8dpviy-tlI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)