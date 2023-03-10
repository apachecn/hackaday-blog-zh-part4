# 用 Arduino 驱动三色电子纸价格标签

> 原文：<https://hackaday.com/2022/10/28/driving-three-color-e-paper-pricetags-with-an-arduino/>

ePaper pricetags 作为一种修补技术的廉价方式，正在成为黑客社区中流行的部分。[Aaron Christophel]得到了一款 4.4 英寸的红色、黑色和白色型号，[并开始编写一款 ESP32 来提高价格。](https://www.youtube.com/watch?v=sWKEWG-0ZLE)

显示器使用的协议是逆向工程，通过射频提示显示器更新，并监控发送到显示器控制板的微控制器之间的信号。一旦理解了协议，就可以移除其中一个微控制器，用一个 ESP32 代替，进行直接控制。实现这一点需要一些拆卸和一些微妙的焊接，但这并不应该吓跑一个有经验的黑客。

有了闪入 ESP32 的正确代码，[如 Github 上可用，](https://github.com/atc1441/E-Paper_Pricetags)可以直接运行显示。黑客代码在驱动显示器方面做得很好，显示出清晰的线条和干净的颜色，表明电子纸显示器运行正常。

我们以前见过[Aaron]在这方面的工作，当他破解更简单的双色电子墨水价格标签时。他甚至用回收的展示品创作了整面墙的展示品[，这是一个相当壮观的场景](https://hackaday.com/2022/08/05/e-paper-price-tags-combined-to-create-a-large-wireless-display/)。休息后的视频。

 [https://www.youtube.com/embed/sWKEWG-0ZLE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sWKEWG-0ZLE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

