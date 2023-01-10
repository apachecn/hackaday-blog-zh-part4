# 完善 3D 打印相机运动控制装备

> 原文：<https://hackaday.com/2021/05/21/perfecting-a-3d-printed-camera-motion-control-rig/>

如果你曾经看过那些高制作价值的 YouTube 视频之一，并想知道他们如何能够获得那些相机似乎围绕着一个物体旋转的平滑镜头，你可能正在看一个电动相机运动系统的产品。毫无疑问，这些设备可以产生视觉上引人注目的照片，但它们的高成本通常使它们无法进入我们这些低级黑客的手中。

当然，除非你真的喜欢[安迪]，并建立自己的。[这款令人印象深刻的钻机的最新版本](https://hackaday.io/project/179800-motion-control-rig-010)具有连续旋转的能力，这要归功于商用的 12 线滑环和光学终点挡板，因此机器在移动开始时仍然可以归位。板载 Raspberry Pi 和 Arduino Uno 负责控制步进电机，其配置最终让人想起标准的 3D 打印机。

[![](img/f2c5c2656c3db80102abc975a3d8519c.png)](https://hackaday.com/wp-content/uploads/2021/05/motionrig_detail.jpg)

The MQTT remote can hold a phone for live video.

[Andy]开发的软件可以让他将相机与他建造的小型旋转平台同步，这样就可以拍摄更复杂的照片，如下面的视频所示。它还支持一个非常漂亮的支持 MQTT 的遥控器，这是他在之前的项目中制作的，这使得直接控制相机和监控其状态变得更加容易。

想给自己的项目视频添加一点润色吗？[安迪]已经发布了所有的文件和信息，你需要建立自己版本的运动控制装置，尽管我们不会责怪你对这个感到有点害怕。它可能不是我们见过的最复杂的相机运动控制系统，但它肯定是最好的。如果你只是想要一个高架视频，不需要那些花哨的跟踪拍摄，[也许一个改良的 VESA 手臂会符合要求](https://hackaday.com/2021/02/08/vesa-arm-turned-low-cost-overhead-camera-rig/)。

 [https://www.youtube.com/embed/IlbN-H5FYP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IlbN-H5FYP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

