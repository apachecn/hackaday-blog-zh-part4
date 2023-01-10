# LED 花束是容光焕发的黑客桌面装饰

> 原文：<https://hackaday.com/2022/03/15/led-flower-bouquet-is-a-radiant-hacker-desk-decoration/>

[Jeremy Cook]给我们写了他的一个项目-[一束 LED 立方体花](https://www.youtube.com/watch?v=bSHHZt1QaZ8)。这些花是由小的城堡状 PCB 制成的 PCB 立方体，每个立方体的中心都有一个可单独寻址的 LED。城堡用机械方式将立方体固定在一起，由于巧妙选择的引脚排列，只需要订购两种不同的 PCB 就可以建造这样一朵花！

作为这些花的花瓶，他决定使用玻璃瓶——这需要一个切口来适应 ESP8266 供电的 NodeMCU 板，这是该项目的控制器选择。在几个不同的切割玻璃的方法都导致瓶子破裂后，他放弃了“干净切割”的想法，重新使用了一个破碎的瓶子，将它粘好，以达到美观的效果。

[Jeremy]告诉我们，他得到了我们在 2017 年报道的[黑客的帮助——使用二极管进行电平转换，因为 ESP8266 的 3.3 V 电平信号与 WS2812 输入不匹配。由此，用于 ESP8266 的 WLED 固件将一切完美地结合在一起。很明显,[Jeremy]花了一整天来设计这个，玩弄所有的想法和方法！](https://hackaday.com/2017/01/20/cheating-at-5v-ws2812-control-to-use-a-3-3v-data-line/)

五颜六色的 led 是装修黑客家的必备。从一束花中，你可能会发现自己正在绘制一个城堡状 PCB 瓷砖设计，接下来你知道的是，你已经[创建了一个漂亮的 LED 三角形瓷砖系统](https://hackaday.com/2021/06/07/triangle-tiles-form-blinky-networks-using-clever-interconnects/)。一些 PCB 工厂嘲笑城堡，如果是这样的话，你[还不如自己完成任务](https://hackaday.com/2021/12/11/snip-your-way-to-diy-pcb-castellations/)。

 [https://www.youtube.com/embed/bSHHZt1QaZ8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bSHHZt1QaZ8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

