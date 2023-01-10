# 马自达的宏

> 原文：<https://hackaday.com/2020/06/23/macros-for-a-mazda/>

[Arik Yavilevich]最近升级了他的第二代马自达的控制台，从股票繁忙盒变成了一个 Android 主机，在一个漂亮的大触摸屏上完成所有操作。它还可以从方便的方向盘按钮上接收输入——这是一个很好的选择，可以让你的眼睛盯着路面，偶尔在电台突然改变时吓到你不知情的乘客。

唯一的问题是[Arik]的股票方向盘上没有任何媒体专用按钮。在短暂的垃圾场之旅后，[Arik]有了一个更好的轮子来搭配新的头部装置。

[Arik]不使用巡航控制，这些特殊的按钮无法通过重新编程汽车的计算机连接起来，所以[他使用藏在手套箱中的 STM32 黑色药丸板，将它们制作成通过蓝牙控制主机](https://blog.yavilevich.com/2020/06/repurposing-unused-steering-wheel-buttons-as-generic-macros-for-an-android-head-unit/)的宏按钮。

[Arik]发现巡航控制按钮不通过 CAN 总线，而是使用电阻梯/分压器，直接连接到 ECU。之后，主要是找到正确的电线，然后切割和重新布线，使按钮在 ACC 设置和 on 上工作。休息过后是一段简短的演示视频。

有一部旧的智能手机吗？你当然知道。为什么不制作自己的头单元呢？

 [https://www.youtube.com/embed/MuFowEPcP0U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MuFowEPcP0U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



道具以【刺猬】为尖！