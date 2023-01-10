# 用微控制器把一个廉价的动作摄像头改装成仪表板摄像头

> 原文：<https://hackaday.com/2020/09/25/hacking-a-cheap-action-cam-into-a-dashcam-with-a-microcontroller/>

改变商品电子产品的用途是真正的黑客形式之一，而且总是简单的小黑客导致大黑客。[Everett]想要使用一个 20 美元的 GoPro 克隆作为仪表板摄像头，所以他给它连接了一个微控制器，使一些动作自动化，并使它变得实用。

当连接到汽车充电器等外部电源时，相机会自动打开，但开始和停止录制以及关机都必须手动完成。[Everett]想要自动化这些功能，所以他打开相机，开始用示波器探测。他发现电源按钮，录音按钮，3.3 V 和外部 5 V 的痕迹，方便地在相机的顶部彼此相邻。

为了实现所需功能的自动化，他在一个小型分线板上连接了一个 PIC10，由 3.3 V 线供电。启动时，它会检测 5 V 电压是否通过 N 沟道 FET 连接到充电端口，然后自动开始记录。当随车关闭 5 V 电源时，它会等待 10 秒钟，然后停止录制并关闭摄像机。如果在启动时没有检测到外部 5 V 电压，微控制器什么也不做，这允许相机被用作普通手持设备。[Everett]用 3D 打印机和 3D 笔组合而成的磁性支架将相机安装在后视镜上。

这是一个简单实用的小黑客，固件在 [Github](https://github.com/tterev3/dash-cam-controller) 上有。廉价的 dashcams 也有类似的价格，但你不会得到任何黑客的满足感。

行动相机的本质激发了黑客行为。你可以在 3D 打印机的帮助下简单地添加一个外部电池，或者全力以赴从头开始建造一个 T2 万向头盔摄像头

 [https://www.youtube.com/embed/Z63TLV2uCO0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Z63TLV2uCO0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

