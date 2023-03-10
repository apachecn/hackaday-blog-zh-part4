# 树莓派抓住了早起的鸟儿

> 原文：<https://hackaday.com/2019/07/04/raspberry-pi-catches-the-early-bird/>

如果你住在一个鸟类活动频繁的地区，设置一个喂鸟器，看着一些饥饿的小家伙来访，你会是一个很好的放松的消遣。扔进一个带有一些传感器的树莓派，它也可以成为你下一个物联网项目的开始，就像[sbkirby]的[喂鸟器监控项目](https://www.instructables.com/id/Bird-Feeder-Monitor-V20/)一样。

为了跟踪鸟类访客的到达和离开时间，[sbkirby]在喂鸟器的两侧安装了一组电容触摸传感器，并通过 CAP1188 分线板将它们连接到 Raspberry Pi Zero W。数据通过 MQTT 发布到另一个充当后端并存储数据的 Raspberry Pi，以及一个可选的额外配备摄像头的 Pi，该 Pi 将沿途为每个客人拍照。考虑到降水可能会影响传感器读数，他还会检查当前的天气情况，以在必要时重新校准传感器，并根据天气情况观察鸟类的存在和进食行为的变化。

似乎基于传感器的动物喂食将永远成为一些新项目的灵感来源，无论是喂食动物本身是目标，就像最近的[这个喂鱼器显示的](https://hackaday.com/2019/07/02/this-arduino-is-feeding-the-fishes/)，还是进食行为被监控并用于进一步的研究，比如[这个基于松鼠的天气预报系统](https://hackaday.com/2016/07/28/squirrel-cafe-to-predict-the-weather-from-customer-data/)。