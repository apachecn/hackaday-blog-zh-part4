# 快速和肮脏:通过电报操作对讲机

> 原文：<https://hackaday.com/2019/12/02/quick-and-dirty-operate-an-intercom-via-telegram/>

永远不要低估快速和肮脏的黑客。无论你手头有什么，快速解决一个真实的问题是非常令人满意的，并且有助于保持你的黑客技能对于那些大的漂亮的工程项目是敏锐的。[Guillaume M]需要一种方法来远程打开他的公寓大楼的门进行递送，所以他入侵了通过电报操作的[古代对讲机，以允许包裹安全地存放在他在大楼正面的邮箱中。](https://www.gmsec.fr/blog/hacking-my-intercom-with-remote-door-opening-functionality-and-more)

[Guillaume]需要以一种允许他在离开时将对讲机恢复到原始状态的方式来完成入侵。打开这个有 30 年历史的单元，他探测了一排螺丝端子，确定了一个 13V 的电源、地线以及与大楼门锁的连接。他将锁终端连接到一个继电器上，继电器由一个树莓 Pi Zero W 控制，等待“打开”命令发送到一个定制的电报机器人。

为了给 Pi 供电，[Guillaume]通过分压电路将它连接到对讲机上的 13V 电源。分压器通常是糟糕的电源，因为输出电压会随着负载的变化而波动，但看起来它对[Guillaume]来说足够好了。对讲机内部有很多空间，所以测试后所有东西都装在外壳内。

如果你想用 ESP8266 达到同样的效果，[有一个库可以满足你的需求。请记住，依赖网络服务器打开关键的大门](https://hackaday.com/2019/02/21/talking-telegram-with-the-esp8266/)[可能会让你被锁在外面](https://hackaday.com/2017/04/05/iot-startup-bricks-customers-garage-door-intentionally/)。