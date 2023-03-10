# 寻日日晷可以立即自行校准

> 原文：<https://hackaday.com/2020/05/06/sun-seeking-sundial-self-calibrates-in-no-time/>

日晷是人类最古老的报时方式之一，是典型的永久性装置。一个很好的理由是，太阳以任何精度显示时间都需要二维校准——一次用于基本方向，另一次用于当地纬度。

[poblocki1982]是一名业余天文学家和半职业日晷爱好者，他花时间制作了一个自动校准的赤道表盘，可以在阳光照耀的任何地方使用。这种太阳美景只需要一个水平的表面和几秒钟的时间来找到它的方位。

打开它，放下它，日晷在一个连续旋转的伺服系统上旋转，直到 HMC5883L 罗盘模块找到南北方向。然后 GPS 模块确定纬度，一个 180°的伺服平移盘子，直到找到理想的位置。一切都由 Arduino Nano 控制，并由 9V 电池供电，尽管我们希望有一天能看到它由太阳能供电。或者会不会飞得离太阳太近？在休息后的简短演示中，看看这个东西自我校准的速度有多快。

对你来说不够便携？这是你戴在手腕上的反向日晷。