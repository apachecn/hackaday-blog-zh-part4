# 学习优化汇编代码…用于 Android

> 原文：<https://hackaday.com/2018/10/30/learn-to-optimize-code-in-assembly-for-android/>

在对微控制器编程时，你会比对现代计算机编程更早地遇到一些物理限制，无论是程序大小还是处理器速度。为了充分利用一个小芯片，我们可以很容易地钻研汇编语言来优化我们的代码。另一方面，与微控制器相比，日常电脑和智能手机中的现代处理器速度如此之快，内存如此之大，以至于这很少是必要的，但如果你真的想深入研究用于 ARM 的汇编语言，那么[Uri Shaked]有一个教程可以帮助你入门。

教程从一个完全用汇编语言编写的 Android“hello，world”程序开始。[Uri]详细介绍了程序的每一行，因为如果你以前从未接触过汇编，它看起来会有点混乱。该计划的后半部分是如何通过使用 Android 原生开发套件(NDK)和使用 ADB 与手机通信在您的设备上实际执行该程序的演练。对于我们中的一些人来说，这可能已经是第二天性了，但对于那些以前从未在手持设备上编程的人来说，值得注意的是，与普通计算机相比，需要经历更多的步骤。

如果你想跳过汇编语言部分，直接开始为 Android 编写程序，你可以下载一个 IDE 并很容易地开始，但是一旦你陷入困境，了解汇编有一个巨大的优势，特别是如果你想开始逆向工程软件或位碰撞通信协议。如果你手边没有 Android 设备可以学习，你仍然可以通过玩游戏来学习汇编。