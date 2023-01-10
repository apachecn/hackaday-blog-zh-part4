# 电信古玩侵入简单的柜台

> 原文：<https://hackaday.com/2020/05/26/telco-curio-hacked-into-simple-counter/>

tikkenteller 是一种用来测量电话使用时长的设备。70 伏特的电压以 50 赫兹的频率通过电话线传输，以运行一个机电计数器，这种设备通常用于几个用户共用一部电话的公共区域。[【查尔斯·巴巴奇】决定将这个 20 世纪 50 年代的结实的五金器具改造成一个简单的柜台。](https://www.youtube.com/watch?v=D_D3LM-WEwQ&feature=youtu.be)

当从 tikkenteller 的按钮接收输入时，构建使用 ATtiny13 为原始硬件生成脉冲。一个固态继电器由微控制器触发，微控制器将原来的螺线管连接到主电源以点动计数器。一个 HLK-PM01 5V 电源用于运行微，允许整个项目运行一个单一的电源。

这是一个巨大、沉重、美丽的金属块，建造风格我们再也看不到了。这绝不是你能建造的最便宜或最有效的柜台，但它有一种你在更现代的硬件上找不到的魅力。你可以使用这样的设备来跟踪你的 Youtube 用户，也就是说… [如果 API 没有为每个人打破这个记录的话。](https://hackaday.com/2019/08/01/a-farewell-to-youtube-sub-counters-set-to-break-with-api-change/)休息后的视频。

 [https://www.youtube.com/embed/D_D3LM-WEwQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/D_D3LM-WEwQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

