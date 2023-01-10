# 用最简单的方法建造一个 DSLR 摄影亭

> 原文：<https://hackaday.com/2019/12/22/build-a-dslr-photo-booth-the-easy-way/>

在资本主义社会，众所周知，任何产品或服务，如果用于婚礼，成本会立即增加两倍。为了避免在朋友的大喜日子花大价钱买一个简单的照相亭， [[Lewis]决定自己建一个。](https://www.instructables.com/id/Arduino-Wedding-Photo-Booth-3D-Printed-Parts-Autom/)

想要高质量的照片输出，佳能 DSLR 被选中执行摄影任务。一台 Arduino Nano 随后投入使用，负责演出。它连接到一个 MAX7219 LED 矩阵，向自愿参与者提供指令，参与者通过一个巨大的发光按钮激活系统。当按下时，Nano 等待十秒钟并触发相机快门，这样做三次。图像显示在连接到相机的 ~~USB~~ HDMI 端口的屏幕上。

这是一个让事情变得简单的构建。不需要单板电脑，只需要一个摄像头、一个 Arduino 和一个显示器。我们确信参加婚礼的人过得很开心，我们期待看到刘易斯接下来会有什么样的表现。我们以前也在这里见过他的一些手下。

 [https://www.youtube.com/embed/Fu5Gbpv4EYs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Fu5Gbpv4EYs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

