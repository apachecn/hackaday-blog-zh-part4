# 触摸屏回流焊炉拉出所有停止

> 原文：<https://hackaday.com/2020/07/16/touch-screen-reflow-oven-pulls-out-all-the-stops/>

我们已经见过很多简单的回流焊炉，很有可能一些读到这些文字的人甚至已经自己组装好了。一个最小的例子不过是一个旧的烤箱、一个固态继电器(SSR)、一个热电偶和一个微控制器，让它们都能说话。但是，如果你像[癞皮狗]一样，愿意付出更多的努力，最终的结果可能会是一件让黑客空间羡慕的设备。

这个建筑和大多数建筑一样，从寻找一个用过的烤面包机开始。但最终他发现了一个德国型号，足够便宜，他可以买新的，而不会超出项目预算。尽管他很快发现了原因:当它到达时，所谓的“披萨烤箱”比他想象的要小得多。幸运的是，它最终成为多氯联苯的完美尺寸。

不幸的是，加热元件不在他想要的地方。他说，即使在用陶瓷隔热材料包裹加热室之后，温度也只会每秒上升 1 度。这一特征很可能是为了降低成本而从最初的烤箱中去掉的。因此，他在烤箱顶部增加了一个额外的卤素加热元件，将速率提高到每秒 6 度。

控制由 Arduino Pro Mini 和带有一些非常光滑的图形的触摸屏显示器提供。有一个预期的热电偶来检测当前温度，但尽管早期版本的电子产品使用上述 SSR 来控制加热元件，但[Mangy_Dog]最终用额定 4000 瓦的调光模块取代了它。在想出一个允许他用 Arduino 控制调光器的电路后，这个模块对室温进行了更精细的控制。此外，很明显，当各种因素 100%发挥作用时，它让他家所有的灯都不会闪烁，这是一个不错的奖励。

[这不是我们第一次看到](https://hackaday.com/2015/11/28/the-internet-of-reflow-ovens/)有人[把液晶显示器塞进现成的烤面包机](https://hackaday.com/2019/03/10/diy-reflow-oven-is-heavily-documented/)，但这无疑是我们遇到的最完美的例子之一。[当即使是商用设备也需要一些黑客技术](https://hackaday.com/2019/07/11/a-drop-in-controller-replacement-for-commercial-reflow-ovens/)才能达到与 DIY 版本同等的功能时，建造自己的回流炉似乎仍然是 2020 年的趋势。

 [https://www.youtube.com/embed/BncBolIe5Jo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BncBolIe5Jo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

