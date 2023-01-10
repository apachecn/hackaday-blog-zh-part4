# 构建具有高级功能的自行车仪表板摄像头

> 原文：<https://hackaday.com/2021/11/01/building-a-bicycle-dash-cam-with-advanced-capabilites/>

骑自行车是一种既美妙又健康的出行方式。然而，就像路上的任何其他车辆一样，有一个摄像头来记录交通状况是很有用的。理查德·奥黛特建造了这样一个钻机。

最初的设置依赖于 Raspberry Pi 3，它使用附加的 Pi 相机每 10 秒拍摄一张照片。然后，它使用 OpenALPR 处理这些照片，OpenALPR 是一种用于读取车牌的软件。骑自行车时检测到的车牌可以存储在树莓 Pi 上以备后用，这在发生事故时会很有用。

然而，从那以后，[理查德]进一步发展了这个概念。修改后的 dashcam 增加了盲点检测以增加安全性，并使用了 Luxonis OAK-D 相机，该相机提供立体深度数据并具有 AI 加速功能。它与背包中的笔记本电脑配对，而不是树莓派，可以将视频传输到放在车把上的智能手机上，作为一种后视镜。

任何骑自行车上下班的人都会立即看到像[Richard]这样的工作的价值。仅仅是避免一场来自后面的汽车的事故就具有巨大的价值，我们几乎很惊讶我们在野外没有看到更多的自行车后视套件。

或者，如果你只是想在骑车时扫描你的周围环境，[考虑建造一个风景扫描仪来代替](https://hackaday.com/2021/09/27/put-a-landscape-scanner-on-your-bike-and-ride/)。休息后的视频。

 [https://www.youtube.com/embed/zMTRDsA6uJM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zMTRDsA6uJM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

