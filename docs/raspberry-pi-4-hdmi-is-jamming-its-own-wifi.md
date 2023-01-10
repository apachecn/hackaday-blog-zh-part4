# 树莓 Pi 4 HDMI 正在干扰自己的 WiFi

> 原文：<https://hackaday.com/2019/11/28/raspberry-pi-4-hdmi-is-jamming-its-own-wifi/>

对流行的产品线进行升级听起来可能是个好主意，但是向现有产品添加更大/更好/更快的部件可能会导致无法预见的问题。例如，在现有的汽车平台上安装一个更强大的发动机起初可能看起来有效，直到人们开始报告扭矩增加导致车架弯曲。在树莓派的世界里，似乎是[Pi 4 中的“升级引擎”在特定情况下](https://www.enricozini.org/blog/2019/himblick/raspberry-pi-4-loses-wifi-at-2560x1440-screen-resolution/)导致 WiFi 停止工作。

[Enrico Zini]注意到了这个问题，并试图准确再现导致 WiFi 中断的原因，在测试了各种 Pi 4 板、电源、操作系统版本和大量其他变量后，确定了原因是屏幕分辨率。显然，在使用 HDMI 的 2560×1440 设置下，WiFi 会掉线。虽然你可能认为 SoC 可能无法处理高分辨率、WiFi 和这台微型计算机必须立即处理的所有事情。但是实际原因似乎比简单的系统资源问题更有趣。

[Mike Walters] [在 Twitter 上发了一篇关于这个问题的帖子](https://twitter.com/assortedhackery/status/1200056633898029061?s=19)用 HackRF 四处探测，发现了一个无线电频率问题。结果是，在这个屏幕分辨率下，Pi 4 会发出一些 RF 噪声，正好在 WiFi 通道 1 的范围内。似乎 Pi 4 在自己身上充当 WiFi 干扰器。

这个故事是相当新的，所以希望树莓派基金会意识到这个问题，并致力于纠正。但是现在，如果你遇到这个问题，最好是运行一个稍微低一点的分辨率。