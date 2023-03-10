# 传统的家禽调理是一个愚蠢的方案

> 原文：<https://hackaday.com/2020/10/09/classical-poultry-conditioning-is-a-bird-brained-scheme/>

不久前，[Kutluhan Aktar]试图通过使用一点经典的条件反射来破解他们的鸡、鹌鹑和鸭子，以获得更高的产蛋量和更快的孵化时间。也就是说，每天在同一时间给它们喂食，同时让它们接触声音和光线。一旦[库特鲁汉]滑了足够多的次数，他们就策划了一个建造自动喂食器的计划。

这个有趣的公鸡形状的喂鸟器在 Arduino Nano 上运行，并从 DS3231 RTC 获取时间、日期和温度信息。【库特鲁汉】要做的就是设定每天的喂食时间。当它到来时，一对伺服系统和一个云台组件一起工作，翻转装满食物颗粒的品客薯片罐。压电蜂鸣器和绿色 LED 提供声音和光来帮助调节。从休息时间开始，看看它是如何工作的。

如果库特鲁汉厌倦了每天看着鸟儿在同一时间进食，也许“垃圾换零食”训练计划会是下一个目标。

 [https://www.youtube.com/embed/JFzTOdidwoU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JFzTOdidwoU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通过 [r/duino](https://www.reddit.com/r/arduino/comments/j65u98/arduino_rtc_bird_feeder_v20_for_poultry/)