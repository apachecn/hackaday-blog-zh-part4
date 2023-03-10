# 简易圣诞树圣诞树装饰品

> 原文：<https://hackaday.com/2021/01/01/simple-christmas-tree-christmas-tree-ornament/>

当你唯一的工具是一把锤子时，所有的问题看起来都像钉子。圣诞树上的 LED 装饰品可以用任何简单易行的方法来制作。你当然不需要运行在 120MHz 的 ARM Cortex M4 CPU 满嘴三个字母的功能，如 FPU、ETM、ETB、ECC、RWW、TCM、EIC、AES、CAN 总线等等。但是【马丁·赫尔德】用 [ATSAME51 系列微控制器](https://www.microchip.com/wwwproducts/en/ATSAME51N19A#additional-features)和许多双色 LED 制作了一个超级简单的 LED 圣诞树装饰品。他已经从他更广泛使用的其他项目中获得了该设备的原理图符号和程序员，因此在节日期间及时将它们组装起来对他来说要快得多，尽管事实上除了无源器件之外，微控制器很可能是 BOM 中最便宜的部分。

在这一点上，人们可能会认为使用可寻址 LED(如 WS2812B 或 APA102C)会简单得多。您可以使用更基本的微控制器来驱动它们，而不需要这么多 GPIO 引脚。但是将这种“智能像素”LED 用于手工组装的原型有时会导致意想不到的结果。如果它们不是以密封带/卷的形式储存，那么储存条件会产生不利影响，导致坏像素。而且，它们在焊接前需要特殊的烘烤程序。为家里的几个 led 灯这么做可能会很棘手。

![](img/ceef4a3369d344392f3ed51ffed60c4f.png)因此，对于 LED，他又一次打破常规，选择使用三种不同颜色的双色 LED，易于手工焊接，1206 个尺寸。这使得他可以在完成的装饰品中获得相当随机的颜色组合。

LED 阵列是伪 charlieplexed。每个 LED 的一端连接到微控制器上的 GPIO 引脚，所有 LED 的另一端连接到一对互补的 N 沟道/P 沟道 MOSFETs，以图腾柱方式连接。根据通过 GPIO 引脚将 gate 引脚驱动为高电平或低电平来开启哪个 MOSFET，每个 LED 的第二个引脚连接到电源或地。结合驱动高/低的 GPIO 引脚，这允许双色 LED 在任一方向上偏置。让每个 LED 发出一种颜色非常简单——将所有 LED GPIOs 设置为低电平，MOSFET 栅极 GPIO 设置为高电平将使 LED 向一个方向偏置。反转 GPIO 逻辑，led 将偏向另一个方向。如果做得足够慢，这两种颜色很容易区分。如果驱动逻辑变得很快，每 10 微秒改变一次状态，这两种独立的颜色就会融合成第三种色调。通过一些聪明的代码，他还在 GPIO 输出状态中添加了一些随机性，从而产生了更吸引人的闪烁效果。[Martin]在下面嵌入的视频中进行了详细介绍。

如果您有相同的一堆器件，并希望复制该项目，请注意，KiCad 源文件需要一些工作来清除错误— [Martin]很匆忙，知道自己在做什么，因此原理图中有一些故意的错误，例如对 N 沟道和 P 沟道 MOSFETs 使用相同的符号，用单向 LED 符号代替双向符号。对于编程，你将需要这些昂贵的[弹簧针式电缆](https://www.digikey.com/en/products/detail/tag-connect-llc/TC2030-IDC/4571121)，除非你决定在发送 Gerbers 之前编辑 PCB。

[Martin]只做了三件定制饰品，保留了一件，把另外两件送给了邻居和同事。但是，如果你真的想用可寻址的发光二极管制作一个圣诞树装饰品，那么看看 [Sierpinski 圣诞树](https://hackaday.com/2020/12/04/sierpinski-pcb-christmas-tree/)，它可以级联起来形成一个圣诞树装饰品阵列。

 [https://www.youtube.com/embed/IxqpVh3s76U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IxqpVh3s76U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

