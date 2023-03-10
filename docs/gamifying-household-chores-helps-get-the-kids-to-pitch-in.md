# 将家务活游戏化有助于让孩子们参与进来

> 原文：<https://hackaday.com/2019/06/05/gamifying-household-chores-helps-get-the-kids-to-pitch-in/>

很少有人对做家务感到兴奋。这可能导致家庭成员放弃他们的职责。在这些情况下，强制执行是一种常见的策略。厌倦了层层叠叠的家务表格和不一致的结果， [[alastair-a]决定升级电子家务跟踪系统。](https://www.instructables.com/id/Task-Manager-a-Household-Chore-Management-System/)

[alastair-a]的任务管理器基于一个 Arduino Nano，配有一直流行的 HD44780 兼容 LCD 屏幕。与该单位的接口是通过旋转编码器和 RFID 标签，而一个实时时钟模块跟踪时间。

自定义数据结构用于管理任务。这允许为不同的任务设置不同的频率，以及跟踪不同用户的完成时间。每个用户都有自己的个人 RFID 标签，可以在阅读器上滑动，以指示家务何时完成。

最初的意图是让设备每周打印报告，以奖励家庭中表现最好的成员。然而，[alastair-a]报告称，这种设备在年轻家庭成员中非常受欢迎，以至于他们似乎完全忘记了奖励！

我们以前见过家务提醒；将其打造为物联网设备通常很受欢迎。