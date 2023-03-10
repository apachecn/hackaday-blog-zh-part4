# 这个比特币价格追踪交通灯不仅仅是一个红色的 LED

> 原文：<https://hackaday.com/2018/11/22/this-bitcoin-price-tracking-traffic-light-isnt-just-a-red-led/>

快，比特币的价格是多少？今天比昨天低吗？你在透支你的兰博基尼账户吗？如果你有一个简单的方法，一眼就能看出如果你在去年 12 月卖出，你能赚多少钱，那会怎么样？[这就是这个比特币价格追踪红绿灯](https://www.balena.io/blog/build-a-bitcoin-traffic-light-with-balenacloud/)的意义所在，它很好地利用了现有的电子设备。

这个构建的硬件是一个交通灯台灯，在亚马逊上售价 20 美元。在这个交通灯里，你会看到一个有三个发光二极管的印刷电路板和一个控制发光二极管的微型控制器。在这种情况下，不使用微控制器，而是移除微控制器，并将几根导线焊接到用于驱动 led 的晶体管的基极。这些电线的另一端连接到树莓 Pi Zero W 上的三个引脚，为这个交通灯台灯提供 Linux 和互联网连接。

在软件方面，我们看到一个 Docker 容器运行一个 Python 脚本，该脚本从 Coindesk 获取最新的比特币价格，并计算与之前获取的比特币价格相比的变化。这些数据被转移到另一个 Python 脚本中，该脚本实际上改变了灯上的 led。

当然，如今一个“比特币价格跟踪交通灯”就像将一个红色 LED 连接到电池上一样简单，如果你觉得特别新奇，你可以添加一个 220ω的电阻。但这是一个执行得如此之好的项目，我们必须向它致敬。