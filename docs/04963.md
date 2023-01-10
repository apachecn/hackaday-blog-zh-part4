# 不要在家里 DIY 这个手术机器人

> 原文：<https://hackaday.com/2020/01/09/dont-diy-this-surgical-robot-at-home/>

几年前，路易斯维尔的 LVL1 黑客空间为无用和不切实际的设备举办了一次黑客马拉松，这个临时的 [Duh-Vinci 手术机器人](http://wiki.lvl1.org/Duh-Vinci_Surgical_Robot)是“成功”成果之一。虽然它不一定是一个应该用于其预期目的的项目，但它的微型设置肯定是一个有趣的项目。

该项目建立在 MeArm 开源机器人和由 Blynk 板控制的摄像机之上。伺服系统连接在每个机械臂的基座上，可以自由旋转。单独的微控制器用于臂和摄像机的电机控制器，部分是由于摄像机电源的电流消耗。远程控制系统运行在 Android 平板电脑上，用于控制每个手臂。

ESP32-Cam 提供的视频输入被配置为 RTSP 流。至于操作，虽然动作不稳定，灵活性有限，但机器人在技术上能够处理尖锐的东西。它的最终设置看起来有点像饥饿的河马遇到手术的疯狂游戏，肯定不会很快出现在手术台上。

 [https://www.youtube.com/embed/cp49GeoozrA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cp49GeoozrA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

