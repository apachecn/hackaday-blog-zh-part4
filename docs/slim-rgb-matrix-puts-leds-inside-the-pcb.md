# 超薄 RGB 矩阵将 led 置于 PCB 内部

> 原文：<https://hackaday.com/2020/12/07/slim-rgb-matrix-puts-leds-inside-the-pcb/>

有时，构建有趣的东西所需要的只是将相同的旧片段以不同的方式组合在一起。[Sayantan Pal]为不起眼的 RGB LED 矩阵做了这件事，通过将 WS2812b NeoPixel LEDs 嵌入 PCB 中[创造了一个超薄版本。](https://hackaday.io/project/175911-worlds-slimmest-neopixel-led-matrix)

现在流行的 WS2812B 的高度是 1.6 mm，恰好是最常用的 PCB 厚度。使用[EasyEDA](https://hackaday.com/2017/12/05/easyeda-two-years-later/),【say antan】设计了一个 8×8 矩阵，采用了改进的 WS2812B 封装。添加了一个略小的切口，为 led 创造了一个摩擦配合，焊盘被移动到切口外面的面板背面，它们的分配被翻转。PCB 面朝下组装，所有焊盘都是手工焊接的。不幸的是，这产生了相当大的焊料桥，这稍微增加了面板的总厚度，并且可能也不适合用传统的取放组件来生产。

我们已经看到了一些使用[多层 PCB](https://hackaday.com/2019/01/18/oreo-construction-hiding-your-components-inside-the-pcb/)的 PCB 组件的类似方法。制造商甚至开始[将元件嵌入多层印刷电路板](https://hackaday.com/2017/09/11/the-components-are-inside-the-circuit-board/)。

 [https://www.youtube.com/embed/TbOg8Cmzf6g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TbOg8Cmzf6g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

