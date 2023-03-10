# 2022 年徽章:电动势潮汐

> 原文：<https://hackaday.com/2022/07/08/badges-of-2022-emf-tidal/>

当我们慢慢回到一个夏天，在田野里聚会庆祝我们的 hackery 节日时，是时候看看今年的另一批徽章了。英国的电磁场(EMF)通常是两年一次的活动，但由于疫情，它在四年缺席后于今年回归。[EMF 2022 徽章](https://badge.emfcamp.org/wiki/TiDAL)与之前的产品不同，掌上游戏机的外形消失了，取而代之的是一个细长的 USB-C 棒，向第一代波浪形 EMF 徽章致敬。

 [![The text is a little small on the tiny screen.](img/d486f780f14b796903ca001f9f11a504.png "emf-tidal-interface")](https://i0.wp.com/hackaday.com/wp-content/uploads/2022/07/emf-tidal-interface.jpg?ssl=1) The text is a little small on the tiny screen. [![On the rear is this pattern.](img/151d45c1c4b5a6d36c12aa174b97586d.png "emf-tidal-rear")](https://i0.wp.com/hackaday.com/wp-content/uploads/2022/07/emf-tidal-rear.jpg?ssl=1) On the rear is this pattern.

从物理上来说，徽章由两个 PCB 组成，它们插在一起，中间夹着 LiPo 电池，上面的一个携带显示器和电池，而下面的则包含 ESP32-S3 MCU 和各种外设。其中包括一个 QMA7981 加速度计、一个 QMC7983 磁力计，也许最有趣的是一个 ATECC108A 加密加速器。最后一个组件使它有可能成为双因素认证密钥，我们认为这可能是徽章的第一个。

在使用中，TFT 显示器和操纵杆界面是可用的，但对于一个黑客抄写员来说很难读懂，因为他的眼睛可能没有以前那么锐利了。编程是通过 MicroPython 进行的，通过相同的[在线孵化系统](https://2022.badge.emfcamp.org/)使用一种应用程序格式，这将为其他欧洲徽章的所有者所熟悉。已经有相当多的应用程序，我们希望这将有助于这个徽章有一些寿命。

这只是一长串 EMF 徽章中的最新一个，其中[2016 版](https://hackaday.com/2016/08/09/tilda-mk%cf%80-the-emf-camp-2016-badge/)可能是我们最喜欢的。