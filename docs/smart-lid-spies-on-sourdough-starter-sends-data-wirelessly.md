# 智能盖子监视酸奶发酵剂，无线发送数据

> 原文：<https://hackaday.com/2021/03/04/smart-lid-spies-on-sourdough-starter-sends-data-wirelessly/>

[Justin Lam]为他的 [Smart Sourdough Lid](https://www.justinmklam.com/posts/2021/02/levain-monitor/) 项目写了一份非常详细的记录，这是出于获得关于他的 Sourdough 发酵剂的进展和健康的更好数据的愿望，并且更有效地这样做。结果是一个整洁的一体式盖子，可以持续测量罐中发酵剂的温度、湿度和高度。数据通过无线传输进行分析，但盖子顶部还有一个方便的有机发光二极管显示器，可以立即显示有用的数据，如起动机达到峰值多少，以及从达到峰值起已经过了多长时间。

[![](img/37f020076bf338182eebe48d2db5e024.png)](https://hackaday.com/wp-content/uploads/2021/03/IMG_4185.jpg)

The PCB was optimized for size, and not designed with mounting in mind, so a hot-glued machine screw serves as a “button extender”. Issues like this can happen when enclosures are designed after the fact; it’s something to which we can all relate.

我们真的很喜欢设计的专注程度，以及[Justin]解释他的设计决策和描述这些决策的详细程度。毕竟，这不是[贾斯汀]第一次尝试获取关于他的酸面团的数据。我们记得[他早期使用计算机视觉来分析酸面团发酵剂的工作](https://hackaday.com/2018/06/27/raspberry-pi-tracks-starter-fermentation-for-optimized-sourdough/)，他用他所学到的知识来指导这个新的设计；smart lid 更易于使用，处理数据的效率也更高。

这个项目的 GitHub 资源库拥有构建自己的资源库所需的所有信息。lid 基于 ESP8266，集成了一个 VL6180X 飞行时间(ToF)距离传感器、用于检测温度和湿度的 DHT22 和一个用于显示数据的小型 SSD1306 有机发光二极管显示器。小型定制 PCB 保持模块整洁，3D 打印定制外壳使其成为一个整洁的封装。

[Justin]还分析了他获得的结果，并在他的文章的最后部分谈到了这些结果的意义，所以如果你对烘焙感兴趣，并对他的发现感兴趣，一定要看一看。