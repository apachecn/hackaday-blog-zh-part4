# 由多氯联苯制成的 RGB 眼镜

> 原文：<https://hackaday.com/2021/01/16/rgb-glasses-built-from-pcbs/>

百叶窗曾经很酷，但如果你真的想脱颖而出，就很难越过你脸正中间的过于明亮的发光二极管。实现这一点的一个很好的方法是像 Arnov Sharma 那样，制作一副 RGB 眼镜。

该设计智能地利用 PCB 来形成眼镜的整个结构。一个 PCB 构成了眼镜的左臂，带有一个 ESP12F 微控制器和必要的支持电路。它通过一个插槽安装在前面的 PCB 上，并焊接到位。WS2812B LEDs 的 V+、GND 和数据连接也用作机械连接。眼镜的右臂以相同的方式固定，与左臂 PCB 相同，只是没有组装。还用了一点胶水来加强连接。

这是一个整洁的建筑，可以通过智能手机轻松控制，因为 ESP12F 运行一个基本的网络服务器，允许改变眼镜的颜色。这也不是我们第一次看到炫丽的 LED 灯罩了！休息后的视频。

 [https://www.youtube.com/embed/X9MjRa_ybeQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/X9MjRa_ybeQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

