# 自主地效飞行器演示器旨在加速海上运输

> 原文：<https://hackaday.com/2021/10/10/autonomous-ground-effect-vehicle-demonstrator-aims-to-speed-up-maritime-shipping/>

地效飞行器(ekranoplans)的优势是比普通飞机更有效，比船只更快，但迄今为止还没有开发出实验原型。幸运的是，这并没有阻止公司的尝试，这导致了[ThinkFlight]和[rctestflight]之间的合作，为[飞行船公司](https://flyingship.co/)创建了一个[小型演示器](https://www.youtube.com/watch?v=S-eND8-AZFI)。

飞行船公司希望使用无人驾驶电动 ekranoplans 作为高速海上货运载体，可以利用现有的海上基础设施进行装卸。对于比例模型，[rctestflight]负责电子设备和软件，而[ThinkFlight]建造机身。和他之前的 ekranoplan build 一样，【ThinkFlight】在 XFLR5 中设计了它，用数控热线切割机(我们仍然想更好地观察它)从泡沫中切割零件，[用凯夫拉尔](https://www.youtube.com/watch?v=_jJKR8cdHO0)层压它以增加强度。地效飞行器面临的挑战之一是，当它们离开地面效应时，压力中心将向后移动，导致它们上仰。为了在进入和离开地面时保持控制效果，这些飞行器通常在尾部使用一个大的水平稳定器。

这个演示器的一个主要特点是使用安装在底部的激光雷达传感器进行自动高度控制。这是由[rctestflight]使用一个简单的泡沫板 ekranoplan 和[[想想 Flighs]以前的机身](https://www.youtube.com/watch?v=3heh9swH2Zw&t=12s)开发的，并在 ArduPilot 中添加了一些定制代码。它在平滑平静的水面上工作得非常好，但是波浪会将大量噪声引入激光雷达数据。看起来他们能够克服这个挑战，并在平静和恶劣的条件下完成了几次成功的试飞。

最终产品看起来不错，飞行平稳，并且易于控制，因为飞行员不需要担心俯仰或油门控制。“飞舟”能否克服挑战，成为一艘成功的商业飞船还有待观察，我们将密切关注该项目。

 [https://www.youtube.com/embed/S-eND8-AZFI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/S-eND8-AZFI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

