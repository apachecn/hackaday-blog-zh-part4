# 2022 年 FPV 竞赛:ESP32 驱动的 FPV 汽车使用 Javascript 进行 VR 魔术

> 原文：<https://hackaday.com/2022/12/30/2022-fpv-contest-esp32-powered-fpv-car-uses-javascript-for-vr-magic/>

你并不总是需要很多来建立一个 FPV 钻机——尤其是如果你愿意利用现代智能手机的力量。[joe57005]正在展示他的虚拟现实 FPV 模型——一个完全可打印的小型 Mechanum wheels 汽车底盘，配备了一个 ESP32-CAM 板，通过 WiFi 提供 720×720 流。这辆车使用常规的 9g 伺服系统来驱动每个车轮，让你可以全方位移动到你想去的任何地方。如果你的目标是 VR 视图，一个 ESP32 CPU 和一个低分辨率摄像头可能听起来不太像，而 ESP32 所做的只是通过 WebSockets 传输视频流——然而，这种简单性在前端得到了很好的补偿。

由 ESP32 作为客户端 JavaScript 的软件栈，是这个优雅构建的亮点。[joe57005]在项目中使用三星 Gear VR，这是一款便宜但质量不错的“智能手机支架”VR 耳机。ESP32 的摄像头馈送在智能手机的网络浏览器中被转换成一个仿 3D VR 图像，使用称为 WebXR 的技术，使用 WebGL 进行图像变形，并为 HUD 提供普通的 JavaScript 直接触摸控制。所有这些都是开源和公开的，3D 打印文件很快就会成为可打印的——目前，我们获得了 FreeCad 源代码，这已经足够好了。

如果你想要一个可以玩的自给自足的 FPV 平台，可以看看这个——它非常容易访问，投入的软件努力值得学习，如果你曾经想尝试 WebXR，提供的代码应该是一个不错的游乐场。这让我们想起了几年前见过的另一个由 ESP32 驱动的可爱的 FPV 机器人。

有 FPV 的想法吗？我们很想看看，我们也为此举办了一场比赛！不要延迟将其投入使用！

 [https://www.youtube.com/embed/hSHtwTb6PaM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hSHtwTb6PaM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![Hackaday.io FPV Contest](img/9dd2c5a266798df5fd6215c8217b4a5e.png)](https://hackaday.io/contest/188273-2022-fpv-contest)