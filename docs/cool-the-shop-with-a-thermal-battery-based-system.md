# 使用基于热电池的系统为商店降温

> 原文：<https://hackaday.com/2022/01/01/cool-the-shop-with-a-thermal-battery-based-system/>

拥有任何类型的商店都是非常棒的，不管它有多大，也不管它在哪里。如果商店在外屋，你可以制造更多的噪音。另一方面，如果没有某种冷却系统，夏天可能会变得非常热，尤其是如果你没有一扇可以吹微风的窗户(或窗户空调装置)。

[![Five 55-gallon tanks of tap water are buried just outside the shop.](img/e24b8753a7720b17b61da95463ef0d6f.png)](https://hackaday.com/wp-content/uploads/2021/12/thermal-battery-cooling-system-inner.jpeg) 【西雅图的柯蒂斯】[为他的商店建造了一个令人敬畏的基于热电池的冷却系统](https://www.youtube.com/watch?v=j3JvZUGjcq8)。电池部分由五个装满自来水的 55 加仑桶组成，它们串联在一起，埋在地下一英尺，离墙大约两英尺。有两个装满水的散热器，绑在 20 英寸的箱式风扇上——一个在商店内，将热量从商店传递到水中，另一个在外面，将热量从水中传递到凉爽的夜间空气中。大多数夏天，这个 800 平方英尺的商店保持在凉爽的 71 华氏度(21.7 摄氏度)。

我们喜欢将控制器安装在一个旧的电影放映机中。内部有一个 Arduino Uno 在运行，并从四个 DS18B20 单线温度传感器获取输入，用于测量室内、室外、电池和地面温度。通过 LCD 菜单可以进入四种模式——空闲、冷却商店、充电模式和在室外温度骤降时的冻结模式。为什么[西雅图的柯蒂斯]不用防冻剂？太贵了，加上一般不会那么冷。(尽管我们听说西雅图圣诞节下了几英寸的雪。)休息之后再来看看。

如果你不能在你住的地方埋一堆 55 加仑的桶，考虑用乐高建造一个沼泽冷却器。

 [https://www.youtube.com/embed/j3JvZUGjcq8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j3JvZUGjcq8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢提示，[赞阿特金斯]！