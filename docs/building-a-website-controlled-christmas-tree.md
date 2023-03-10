# 建立一个网站控制的圣诞树

> 原文：<https://hackaday.com/2021/01/04/building-a-website-controlled-christmas-tree/>

在过去，圣诞灯是简单的灯丝灯泡串，如果你真的挥霍，你可以得到一些闪光。如今，我们期望我们闪亮的装饰品有更多的功能。[[JT]为自己的圣诞树搭建了一个相当漂亮的网站控制系统。](https://www.instructables.com/Website-Controlled-Christmas-Tree-anyone-Can-Contr/)

这个设置和你可能习惯的版本有点不同。该网站运行在数字海洋上的云托管虚拟机上，而不是在本地运行。这使得网络上的任何人都可以访问该网站，并使用该界面来控制圣诞树上的灯。树的图像被用作界面，并允许用户设置树上每个 LED 的颜色。led 本身由 NodeMCU ESP8266 驱动，它使用其 WiFi 连接来查询网站本身，并根据需要获取颜色数据。[JT]还包括一个辅助界面，Youtube 直播的聊天也可以用来控制 led。

这是一个比大多数典型的在线 LED 闪光灯更复杂的构建，但它教授了在网络上交互和使用虚拟机的有用技能。我们也看到了这种类型的其他版本；[甚至有些是对“圣诞热”本身有反应的](https://hackaday.com/2019/12/24/tiny-tree-is-a-thermometer-for-christmas-fever/)。休息后的视频。

 [https://www.youtube.com/embed/QnCp0fzpeqw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QnCp0fzpeqw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

