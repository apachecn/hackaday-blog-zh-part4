# 为入门级电动汽车增加豪华充电功能

> 原文：<https://hackaday.com/2020/09/12/adding-luxury-charging-features-to-an-entry-level-ev/>

日产 Leaf 是迄今为止有史以来最畅销的电动汽车，这主要归功于它是首批大规模生产的全电动汽车之一。虽然早期进入市场对日产来说很好，但他们没有像其他电动汽车制造商那样进行大量升级，因此开始失去客户。其中一项升级是充电限制，允许在车内设定不同的充电率。不过，经过一些 CAN 总线的修补，[这个特性可以添加到 Leaf](https://github.com/dalathegreat/Nissan-Leaf-ChargeCurrent) 中。

当在不熟悉的或旧的电源插座充电时，限制充电速率是有用的，这些电源插座可能不处理默认充电速率。在欧洲，有一个 240 伏的配电系统，Leafs 将从墙上插座获得大约 3 千瓦的电力，这是相当多的电力。如果插座看起来无法支持这么多的电流，那么降低充电率是很方便的(也更安全),即使给汽车充满电可能需要更长的时间。[Daniel ster]的修改要求用户通过操纵气候控制来设置充电率，因为 Leaf 没有全面的用户界面。

这个项目的核心是通过 CAN 总线执行的，CAN 总线是一种常用的通信方案，常用于车辆中，而且[是有据可查的，很容易利用](https://hackaday.com/2019/05/14/turn-your-car-into-a-simulator/)。幸运的是，[Daniel]已经在他的 GitHub 页面上提供了代码，所以如果你因为 Leaf 缺乏功能而考虑用它来交换其他东西，现在可能是重新考虑的时候了。

 [https://www.youtube.com/embed/u6fHHyJBMu8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u6fHHyJBMu8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



图:[查克艾伦(chucka_nc) / CC BY-SA](https://commons.wikimedia.org/wiki/File:Two_Nissan_Leaf_charging.jpg)