# 今天是星期几？

> 原文：<https://hackaday.com/2020/04/08/what-day-is-it/>

由于目前世界上大多数人都呆在家里，保持我们的理智和一周中的每一天都是一个挑战，特别是没有正常的日常事务可以坚持。为了帮助解决其中的一个问题，[phreakmonkey]建造了一个[日历](https://github.com/phreakmonkey/DayClock)。顾名思义，它的唯一目的是显示今天是星期几。

一个非常简单的设备，两个主要组件是一个伺服和一个 Wemos D1 迷你，流行的基于 ESP8266 的开发板。使用 NTPtimeESP 库，它从互联网上获取星期几，并移动伺服系统以在 3D 打印面上显示当前日期。大多数读者应该能够在一两个小时内快速完成一个，这有助于在这个有趣的时代保持理智。

对于另一个电晕钟，看看[埃利奥特·威廉姆斯]版本的[有助于保持国内和平](https://hackaday.com/2020/03/19/the-corona-clock/)。如果你想做点什么来对抗当前疫情的蔓延，你可以造几个[面罩](https://hackaday.com/2020/03/29/nih-approved-3d-printed-face-shield-design-for-hospitals-running-out-of-ppe/)，把你闲置的电脑拿出来[折叠@家](https://hackaday.com/2020/03/31/behind-the-scenes-of-foldinghome-how-do-you-fight-a-virus-with-distributed-computing/)或者[缝几个口罩](https://hackaday.com/2020/03/18/homemade-masks-in-a-time-of-shortage/)。每一点都有帮助。