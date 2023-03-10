# Arduino 和 Pi 共享电路板空间

> 原文：<https://hackaday.com/2018/12/24/arduino-and-pi-share-boardspace/>

Raspberry Pi Zero (W)和 Arduino 是非常不同的动物，前者具有处理能力和连接性，而后者具有一些模数转换器(ADC)和近乎实时的反应。你可以用一根 USB 线把它们连接起来，对于许多项目来说，这将是两者的完美结合。除此之外，我们可以完全通过串行、SPI、I2C 和逻辑电平信号来连接这种奇怪的耦合。怎么会？通过一个由[cburgess]开发的设备，该设备被称为支持 Pi0 (W) 的 [Arduino 屏蔽。也许这是一个与 Arduino 接口的斗篷。这种区别可能是没有实际意义的，因为每个电路板都有一个熟悉的足迹，两者都可以在这里找到。](https://www.tindie.com/products/cburgess129/raspberry-pi-zero-w-shield-for-arduino/)

根据它们的设置和编程方式，一个可以控制另一个，或者它们可以愉快地做自己的事情，只是交换一点信息。这块板就像树莓派和 Arduino 之间的婚姻顾问。它提供了电平转换，这样他们就不会把对方炸飞，还提供了库，这样他们就可以友好地互相交流。如果你想更深入地研究这个问题，[设计文件和代码示例在](https://github.com/cburgess5294/BurgessWorld/tree/master/Raspberry%20Pi%20Shield%20for%20Arduino)上。

也许我们会在这个板上报道一个[弹球机改造](https://hackaday.com/2018/07/13/mademoiselle-pinball-table-gets-rock-n-roll-makeover/)，一个老式[自动售货机修复](https://hackaday.com/2017/04/30/vintage-vending-machine-makes-the-perfect-gift/)，或者也许是一个来自*回到未来 II* 中复古酒吧的工作道具复制品。