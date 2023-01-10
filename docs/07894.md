# 专为娱乐而打造的 FPGA 视频播放器

> 原文：<https://hackaday.com/2020/09/26/an-fpga-video-player-built-just-for-fun/>

有时，项目是出于需要而产生的；需要解决的问题的解决方案。其他时候，他们只是出于对创造和实验的热爱。[ultraembedded]的 FPGAmp 媒体播放器属于后者，[是一个很好的学习经历。](https://github.com/ultraembedded/FPGAmp)

FPGAmp 的目标是在 Arty A7 开发板上播放各种媒体文件，基于 Xilinx Artix-7 FPGA。它能够以 800 x 600 的分辨率和 25 fps 的速度播放 MJPEG 视频，也能够播放 MP3 和立体声音频。[在 Twitter 上演示该设备](https://twitter.com/ultraembedded/status/1300416716191576064)，[ultraembedded]指出，使用 LED 进行 SPDIF 光学音频输出的方法是不合法的，但确实有效。后来的更新切换到使用 Arty A7 平台的专用音频输出板，[以羊毛衫的一首优秀歌曲为特色。](https://twitter.com/ultraembedded/status/1307654740361256960)

使用 RISC V 处理器内核和硬件 JPEG 解码器，我们想象[ultraembedded]通过这个项目真正提高了他们的 FPGA 技能。[特别是在 ARM 出售给 NVIDIA](https://hackaday.com/2020/09/14/nvidia-acquires-arm-for-40-billion/) 之后，RISC V 继续在硬件社区获得相关性。我们很幸运地在去年的超级电脑展[上做了主题演讲，Megan Wachs 在技术上做了发言](https://hackaday.com/2020/01/27/supercon-keynote-megan-wachs-breaks-down-risc-v/)。休息后的视频。

> 多亏了 [#LVGL](https://twitter.com/hashtag/LVGL?src=hash&ref_src=twsrc%5Etfw) 用户界面库，我的[@ diginentinc](https://twitter.com/DigilentInc?ref_src=twsrc%5Etfw)[# artya 7](https://twitter.com/hashtag/ArtyA7?src=hash&ref_src=twsrc%5Etfw)[# FPGA](https://twitter.com/hashtag/FPGA?src=hash&ref_src=twsrc%5Etfw)媒体播放器项目现在看起来还算不错。播放 800×600 25fps 视频、MP3 和 JPEG 静止图像。Github 上现在提供的所有 RTL 和固件资源:[https://t.co/TTG7huzyZW](https://t.co/TTG7huzyZW)pic.twitter.com/6UWy2UXOfW
> 
> —ultra embedded(@ ultra embedded)[2020 年 9 月 20 日](https://twitter.com/ultraembedded/status/1307654740361256960?ref_src=twsrc%5Etfw)