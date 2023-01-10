# ESP8266 支持的收据打印机将 RESTful API 放在死树上

> 原文：<https://hackaday.com/2021/03/10/esp8266-powered-receipt-printer-puts-restful-api-on-dead-trees/>

将他的数字信息带入现实世界，[Davide Gironi]用一台销售点收据打印机和一台 esp 8266 构建了自己的笔记转录器。

你在餐馆的点餐窗口见过这些收据打印机。一个服务员从餐馆里的任何一台机器上下单，一份书面摘要就会出现，让厨师排队开始(甚至把自己从名单上划掉)。为什么我们自己的生活中不应该有这种便利呢？

打印机使用爱普生打印机标准代码的变体进行通信，[Davide]为此编写了一个库，并令人欣慰地共享了代码。使用几个电压调节器和一些无源元件添加一个 ESP8266 使其成为无线的，除了电源。它有所有有趣的铃铛和哨子来设置 WiFi 凭证，一旦运行，只需按下基座上的按钮，它就会吐出你的数据。

但是，等等，这些数据是从哪里来的？基于 web 的设置页面允许您将 URI 配置到您选择的 RESTful 源代码。(XKCD 有一个，他们没有吗？)它还能让你配置页眉、页脚、错误信息，当然还有你的~~公司~~黑客标志。

我们最喜欢的收据打印机时刻之一是，昔日的一位业余编辑(埃利奥特·菲利普斯)把一台自拍收据打印机带到了 Supercon。我们找不到它的任何照片，所以我们将留给你一个出色的黑客[山姆·泽洛夫]通过将其中一个塞进宝丽来相机完成的。

 [https://www.youtube.com/embed/ecziT1LMRLc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ecziT1LMRLc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

