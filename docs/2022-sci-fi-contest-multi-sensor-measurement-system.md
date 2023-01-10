# 2022 科幻大赛:多传感器测量系统

> 原文：<https://hackaday.com/2022/04/26/2022-sci-fi-contest-multi-sensor-measurement-system/>

许多科幻电影和电视节目都以能够感知各种奇妙事物的手持设备为特色。来自[j]的 Spec Mk II 在很大程度上就是按照这种思路构建的，将大量的功能打包到一个方便的手掌大小的外形中。

ESP32 是该设备的大脑，与 480×320 分辨率的触摸屏相连。板载热感相机，由 MLX90640 传感器提供 32×24 像素分辨率。还有一个 8×8 激光雷达传感器和一个光谱传感器，可以捕捉关于入射光源的各种有趣信息。这也可以用来确定材料的透射系数或反射系数，如果你需要的话。一个 MEMS 麦克风也用于捕捉听觉数据。作为奖励，它也可以画一个 Mandelbrot 集，只是为了好玩。

未来的计划包括添加 SD 卡，以便捕获的数据可以以 CSV 格式存储，以及扩展板载传感器包。这个项目让我们想起了多年来我们看到的一些 [tricorder 构建](https://hackaday.com/2020/08/24/raspberry-pi-makes-a-practical-tricorder/)。休息后的视频。

 [https://www.youtube.com/embed/WwQaEA6qdYY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WwQaEA6qdYY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/YuU9rYVsIoo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YuU9rYVsIoo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![Sci-Fi Contest](img/650ac107d73fa1ba67d57bd366e52230.png)](https://hackaday.io/contest/184314-sci-fi-contest)