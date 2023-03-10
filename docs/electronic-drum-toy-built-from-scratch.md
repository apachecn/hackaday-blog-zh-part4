# 从头开始建造的电子鼓玩具

> 原文：<https://hackaday.com/2022/01/11/electronic-drum-toy-built-from-scratch/>

架子鼓曾经是任何严肃乐队的关键，然而，如今，我们的许多音乐是在电脑上创作的，或者使用架子鼓。[spancac]构建了后者的一个简单例子，使用微控制器构建了一个基本的基于样本的鼓玩具。

该操作的大脑是 STM32F100VET6B，它配有一个用于输出声音的 12 位 DAC。它还有一个健康的 512 KB 的闪存，使它能够在板上存储鼓样本，而不需要额外的部件。样本以 22，050 Hz 的采样速率存储在 16 位分辨率下，即使 DAC 稍后将其削减至 12 位，这对于小型构建来说也是相当不错的质量。

[spanceac]一定会将正确的混音编码到鼓机中，以便触发第二个样本不会停止第一个样本的播放。随着踢，圈套，两个汤姆，和碰撞和乘坐样本船上，有很多得到一个坚实的打击套件。这一切都是建立在一个小的印刷电路板上，用触觉按钮来激活每一种声音。

演示视频显示该套件表现出色；目前还不清楚样本是否存在延迟问题，或者只是因为[spancac]单手游戏的难度。如果是前者，可能只需要在样本开始时进行一些代码调整或简单地修剪静音。总的来说，这是一个整洁的小 groovebox，和其他音乐家一起演奏时使用[非常有趣。](https://hackaday.com/2021/11/23/live-jam-kit-helps-electronic-musicians-stay-in-sync/)休息后的视频。

 <https://hackaday.com/wp-content/uploads/2022/01/143319866-a4ecc4ed-9de9-49c2-8885-e092aff31822.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2022/01/143319866-a4ecc4ed-9de9-49c2-8885-e092aff31822.mp4](https://hackaday.com/wp-content/uploads/2022/01/143319866-a4ecc4ed-9de9-49c2-8885-e092aff31822.mp4)