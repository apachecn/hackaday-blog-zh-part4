# 660 FPS 树莓派视频以极端的慢动作捕捉这一时刻

> 原文：<https://hackaday.com/2019/08/10/660-fps-raspberry-pi-video-captures-the-moment-in-extreme-slo-mo/>

慢动作拍摄早已成为高端智能手机的标准功能，可以将最琐碎的身体活动变成宏伟的动作镜头，在社交媒体上分享。它还揭示了一些隐藏在我们眼前的自然小奇迹:雷暴中闪电的形成，蜂鸟扇动翅膀，或者鳄梨达到成熟的完美时刻。总的来说，这是一种有趣的录制视频的方式，正如[Robert Elder]所展示的，如果你能忍受一些限制，你可以用价值几美元的 Raspberry Pi 设备以高达 660 FPS 的速率做一些事情。

以经典的 24 FPS 为例，这将把一秒钟的视频变成将近半分钟长的慢镜头。为了首先实现这样的帧速率，[Robert]使用[Hermann-SW]的修改版 [`raspiraw`](https://github.com/Hermann-SW/fork-raspiraw) 将原始图像数据直接从相机传感器获取到 Pi 的存储器中，将所有繁重的处理工作留给所有帧被检索后的实际视频。RAM 大小当然是记录长度的一个限制因素，但内存带宽是更大的问题，他使用的更便宜的 6 美元相机型号的分辨率限制在 64×640 像素。是的，64 像素高——但是，嘿，看看那个超宽屏幕宽高比！

虽然你不会从中获得最高的质量，但这仍然是一种令人兴奋和廉价的玩慢动作的方式。不过，你可以随时升级你的游戏，看看这个 DIY 高速相机。嗯，[这是一个安装在剪草机刀片上的](https://hackaday.com/2018/12/28/high-speed-camera-plus-lawnmower-equals-destructive-fun/)破坏除了打印机以外的任何东西。

 [https://www.youtube.com/embed/-gMy8k4nHtw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-gMy8k4nHtw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

