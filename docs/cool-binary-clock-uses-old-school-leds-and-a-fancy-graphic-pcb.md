# 酷二进制时钟使用老派的发光二极管和一个花哨的印刷电路板

> 原文：<https://hackaday.com/2021/08/06/cool-binary-clock-uses-old-school-leds-and-a-fancy-graphic-pcb/>

啊，5 毫米的 LED。它们曾经是流行的选择，但近年来已被更小的 SMD 元件和/或更强大的 RGB 器件所取代。然而，它们仍然能够完成这项工作，并且是给你的项目一个适当的自制外观的好方法。[伊恩·邓恩]选择了这些零件来生产他的 [4017 十进制时钟](https://hackaday.io/project/177594-4017-decade-binary-clock)。

该时钟仅使用数字逻辑 ic 来显示时间，这里没有微控制器！在将近一年的时间里，经过四、五次的反复，伊恩终于能够让电路可靠地运作了。正如你所料，它依靠一个 32.768 kHz 的晶体来提供稳定的时钟。输入到一个 4060 二进制纹波计数器，该时钟被分频 14 倍，以提供一个 2Hz 的方波。然后通过 4027 触发器获得所需的 1Hz 信号。从那里，一堆额外的逻辑处理计数秒，分钟，小时，并重置适当的计数器。

容纳该项目的 PCB 是由一台平板喷墨打印机直接打印的，这是[Ian]受我们之前关于如何在商场制造 PCB 的文章的启发而购买的。在这种情况下，他实际上没有使用它来制作 PCB，但平板打印机在将图形放在板上方面做得很好。

结果是一个相当有吸引力的外观，可能会让一些以前没有见过图形印刷电路板的电子爱好者感到惊讶。我们认为这种技术也可以用在会议徽章上。如果你尝试过类似的技术，请一定给我们写信！