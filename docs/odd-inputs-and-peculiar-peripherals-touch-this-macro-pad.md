# 奇怪的输入和特殊的外设:触摸这个宏键盘

> 原文：<https://hackaday.com/2022/06/13/odd-inputs-and-peculiar-peripherals-touch-this-macro-pad/>

为复杂的软件包提供自定义控件的需求已经以多种方式得到满足，其中最常见的是拥有可配置的键盘。这是一个挑战[Meir Michanie]以稍微不同的方式接受了这个挑战，创造了一个定制的触摸屏宏垫。与按钮不同，这允许在任何配置中使用不同形状的按键进行完全自定义的布局。

它的核心是一个多功能的 ESP32 触摸屏开发板，这种类型的开发板可以在您最喜欢的在线电子市场的页面中轻松找到。Arduino IDE 已被用于设备编程，配置非常简单，只需提供所需布局的 PNG 和定义按钮的 CSV 文件。然后整体通过 BLE 连接，作为键盘呈现给主机。结果是我们见过的最酷的宏面板之一，有无限多的选项。

有了这样一个巧妙的想法，在这些页面上出现的大量宏垫中，可能会有另一个相同想法的出现也就不足为奇了。

[![Odd Inputs and Peculiar Peripherals Contest](img/4c1d0cbefc0219866bf706dbbac40818.png)](https://hackaday.io/contest/185414-odd-inputs-and-peculiar-peripherals)