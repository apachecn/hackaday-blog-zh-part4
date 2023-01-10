# 猫咪喂食器为喵喵组合增加了指标

> 原文：<https://hackaday.com/2019/08/05/cat-feeder-adds-metrics-to-meow-mix/>

如果有一样东西是任何猫都会为之努力的，那就是食物。通常，这只是包括喵喵叫和/或站在你的胸口，直到你放弃货物。有一只漂亮的猫，艾玛，它会在早上的恶心时段大声喵喵叫着要食物。随着年龄的增长，控制体重越来越难，也越来越重要。很明显，是时候建造终极自动喂猫器了——一个可以让他偷懒，同时又能知道艾玛体重的装置。

[经过一年半的工作，进料器完成](https://www.reddit.com/r/3Dprinting/comments/cjsh5c/im_not_sure_if_i_would_spend_15_years_building/)。它不仅每天送货几次，还把一堆关于艾玛饮食习惯的数据发送到云端。平台上有一个秤，食物碗上有一个秤。总的来说，它们提供了大量可以自动上传到 AWS 的指标。一切都由一个 ESP32 Arduino 控制，包括一条彩虹般的 WS2812s，它围绕着喂食器的底座追逐自己的尾巴。速度越快，越接近喂食时间。

这种独特的进料器最好的部分是几乎每个零件都是 3D 打印的，包括齿轮。一定要去看看[建造画廊](https://piotr.westfalewicz.com/blog/2019/07/around-100-printing-hours-later-the-automatic-cat-feeder-emerges/)，在那里你可以看着它一点一点的组装起来。哦，你还可以爬过去看看艾玛被喂饱了。

艾玛不用担心分享她的食物。如果她做到了，也许[DynamicallyInvokable]可以使用[面部识别](https://hackaday.com/2019/01/01/raspberry-pi-raccoon-proof-cat-feeder/)来满足多只猫的需求。

 [https://www.youtube.com/embed/XG0LZ08-GsM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XG0LZ08-GsM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

