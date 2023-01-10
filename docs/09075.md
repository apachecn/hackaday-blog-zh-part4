# 给旧音响添加遥控器

> 原文：<https://hackaday.com/2021/01/29/adding-remote-control-to-an-old-stereo/>

有时候，最好的 hifi 档位是你已经有的档位。在盒式磁带领域尤其如此，因为高质量的走带设备早已停产。[Nick]喜欢他目前的装备，但希望能够在房间的另一端使用遥控器。很自然地，他开始侵入这个功能。

问题中的卡式录音机，雅马哈 K-220，已经老到没有遥控器了，但谢天谢地，它足够新，可以使用电脑控制的磁带传输。这意味着播放、停止、倒带和快进的基本功能都可以通过简单的数字按钮而不是机械按钮来控制。这使得 ATmega328P 很容易与立体声系统的原始电路连接。数字 IO 引脚连接到按钮，大部分时间作为高阻抗输入，只有在需要触发按钮时才切换到地。接下来的简单工作就是将一个红外接收器连接到芯片上，并用一些 Arduino 库对其进行编程，使其与[Nick]身边的典型立体声遥控器配合工作。

这是一个整洁的构建，随着[更酷的](https://ryoshi.bigcartel.com/product/ryo-004-yaw-control) [卡带发行](https://www.shugarecords.com/collections/new-cassettes/products/sufjanstevens-theascension-newcassette2020asthmatickittytape-indierocksynth-pop)每年推出，我们确信【尼克】将在设置上投入一些精力。如果你觉得 IR 太麻烦，你可以更进一步，用一个网络应用来代替它。如果你一直在自己的车间里摆弄类似的东西，[一定要给我们写信！](http://hackaday.com/submit-a-tip)