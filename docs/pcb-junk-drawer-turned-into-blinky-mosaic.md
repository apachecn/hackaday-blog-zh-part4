# PCB 废品抽屉变成了闪亮的马赛克

> 原文：<https://hackaday.com/2018/08/16/pcb-junk-drawer-turned-into-blinky-mosaic/>

我们都有一个装满旧印刷电路板的盒子，就等着被取走任何有用的东西。[Dennis1a4]决定用他的做点什么，把它变成一幅吸引人的镶嵌画，挂在他新工作室的墙上。但这不仅仅是一堆旧电路板:[Dennis1a4]决定使用许多旧电路板上的 led，创建一个闪闪发光的垃圾建筑。这本身就很不错，但他后来决定更进一步，内置一个红外接收器，这样他就可以控制闪烁，以及一个 PIR 传感器，当有人靠近马赛克时，它就会检测到。

整个设置由 ATMega328p 控制，atmega 328 p 驱动几个 PCF8575 端口扩展器，这些扩展器驱动 led。这些以莫尔斯电码模式闪烁。[Dennis1a4]还在其中一块板上使用了一组 DIP 开关来随机化图案，并在另一块板上连接了一个 pizeo 蜂鸣器来发出适当的哔哔声。

 [https://www.youtube.com/embed/G0Am9yqID_s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G0Am9yqID_s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

