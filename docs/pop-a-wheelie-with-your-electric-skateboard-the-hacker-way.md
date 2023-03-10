# 用你的电动滑板弹出一个轮子，黑客的方式

> 原文：<https://hackaday.com/2020/03/20/pop-a-wheelie-with-your-electric-skateboard-the-hacker-way/>

使用一点技术来弥补技能的不足是一个由来已久的传统，否则在那些通过艰苦方式获得技能的人中被称为作弊。学习手动轮滑滑板通常需要花钱，但[blezalex]通过让他的[电动滑板处理平衡动作](https://www.youtube.com/watch?v=pR_RpmM_BDM&t=13s)来解决这个问题。![](img/54b9f907ff6ae28a3003493ddb70575e.png)

乍一看，这个滑板看起来和骑起来就像一个普通的 DIY 电动滑板，有现成的双轮毂电动卡车，VESC 速度控制器和无线油门。当前轮弹出地面时，派对技巧就会出现，这将激活秘密的自平衡模式。此时，STM32F401 开发板和 MPU-6050 IMU 接管对电机的控制，电机通过向前或向后倾斜来控制，就像悬浮板一样。远程油门变成一个安全开关，释放时切断电机电源。

[blezalex]说，在使用这款滑板之前，他一生中只有不到一个小时的滑板时间，这很好地证明了它的效果。最大的挑战是让板在两个轮子上转动，这通过用 IMU 感测板的左右倾斜并向轮子施加比例差分扭矩来解决。稍加练习，你也可以在移动时平稳地在骑行模式之间切换。

我们认为这是一个真正优雅的欺骗，现在我们需要建立一个我们自己的。幸运的是，STM32 固件和指令都在 [GitHub](https://github.com/blezalex/balance_skate) 上。有了[现成的组件，制作自己的电动滑板变得非常简单。](https://hackaday.com/2019/11/22/electric-longboard-quick-build-using-off-the-shelf-components/)我们还见过一种[自行车，它有一个前轮离地作弊装置](https://hackaday.com/2018/09/24/cheating-the-perfect-wheelie-with-sensors-and-servos/)，可以防止你仰面摔倒

 [https://www.youtube.com/embed/pR_RpmM_BDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=1&wmode=transparent](https://www.youtube.com/embed/pR_RpmM_BDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=1&wmode=transparent)

