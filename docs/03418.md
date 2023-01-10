# 桌球大师·博特每次都往酒杯里扔球

> 原文：<https://hackaday.com/2019/06/26/trick-shot-bot-flings-balls-into-wine-glass-every-time/>

我们听说过啤酒乒乓，但我们不确定我们听说过葡萄酒乒乓。当然也从来没有像这样的乒乓球投掷机器人自动化过。

下面的视频中没有太多的细节，也没有构建日志*本身*。但是[电子尘埃]在视频中有几个镜头解释发生了什么，以及在[一个 reddit 帖子](https://www.reddit.com/r/arduino/comments/c462m1/the_trick_shot_machine/)中关于该设备的简短描述。这个想法是将一个球旋转到一个稳定的速度，每次都以同样的方式释放它。钻机本身由木头制成，由普通的刷 DC 电机旋转——[电子粉尘]解释说，他选择它们而不是 PWM 伺服系统，以简化事情，消除释放点的不确定性。球由一对手臂保持，每个手臂由一对业余爱好伺服系统控制。Arduino 和其他东西一起旋转，并在触发伺服系统收回和释放球之前计数 50 转。一旦一切就绪，安置在着陆点的玻璃就能完美地捕捉到球。

这里希望建造细节能很快出现在他的博客上，就像他们为 T2 这个声音反馈杂耍机所做的一样。虽然我们肯定喜欢这个项目，但如果它能把球瞄准玻璃，那可能会很酷。或者它可以一直[在飞行中重新定位目标](https://hackaday.com/2017/03/22/dartboard-watches-your-throw-catches-perfect-bullseyes/)。

 [https://www.youtube.com/embed/Mjwf1dPnljk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Mjwf1dPnljk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

