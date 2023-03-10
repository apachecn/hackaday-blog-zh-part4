# 建立一个 ESP32 股票报价器来观察你的 GME 收益

> 原文：<https://hackaday.com/2021/04/26/build-an-esp32-stock-ticker-to-watch-your-gme-gains/>

如今，迷因投资风靡一时，还有什么比用你自己的老式机械股票报价机来分享损失的乐趣更好的方式呢？不幸的是，它们就像你所期待的维多利亚时代的电子产品一样昂贵和稀有。幸运的是，[【秘密洞穴】已经证明，你可以组装一个功能相似的](https://www.secretbatcave.co.uk/projects/stock-ticker-machine/)，其成本大约相当于 GameStop (GME)股票在登上月球之前的价值。

这似乎是一个雄心勃勃的项目，但实际上这台机器只有几个运动部件。有一个步进电机来进纸，另一个用来旋转着墨的压花轮，还有几个连接在推板上的螺线管。推板不是试图移动沉重的轮子，而是将纸张粉碎。事实上，这产生了令人满意的“噼啪”声，因为每个字符打印只是一个额外的奖励。

[![](img/517c185eaeb41fab2c8163792f8ce66a.png)](https://hackaday.com/wp-content/uploads/2021/04/stockticker_detail2.jpg)

Extending the base to hold the solenoids.

为了推销这种外观，[secretbatcave]将整个装置放入宜家的一个高大的玻璃穹顶内。配套的木制底座被延长，以便推板螺线管可以安装在里面，之后它被浸泡在墨水中，并喷上一层光泽密封剂，以赋予它 20 世纪人们似乎喜欢的闪亮的黑色饰面。加上一个雕刻的黄铜铭牌，这台机器看起来像是从时间扭曲中掉出来的。

在电子方面，有一个 ESP32，一对步进电机控制器，和一个螺线管继电器。截至目前，它都生活在一个相当实用的盒子里，拴在股票上，但我们确信，如果你愿意，可以在定制 PCB 的帮助下，将这些东西塞在底座下。

有了 ESP32 掌舵，跑马灯可以很容易地配置成打印出通过网络接收到的或者从 MQTT 获得的任何数据。有了这样的硬件和一双钻石手，你的手就和你的一样好了。

 [https://www.youtube.com/embed/5EnIKh_EYjg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5EnIKh_EYjg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

