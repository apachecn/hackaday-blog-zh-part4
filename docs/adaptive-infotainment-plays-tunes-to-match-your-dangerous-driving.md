# 自适应信息娱乐系统播放音乐来配合你的危险驾驶

> 原文：<https://hackaday.com/2018/12/29/adaptive-infotainment-plays-tunes-to-match-your-dangerous-driving/>

观看动作片的部分乐趣在于想象自己是主角，总是在进行令人兴奋的冒险，当然，还有完美的配乐陪伴，为你的生活带来刺激和戏剧性。虽然让一个管弦乐队跟着你可能不总是可行的，但[P1kachu]至少知道如何[让一些音乐配器与他如何驾驶他的汽车同步](https://p1kachu.pluggi.fr/project/automotive/2018/12/17/custom-ivi/)，速度与激情的风格。

这个想法非常简单:当[P1kachu]平静而缓慢地驾驶他的汽车时，信息娱乐系统播放的音乐是冷静而含蓄的。但当他放下锤子时，音乐变得更具侵略性，符合新的驾驶风格。虽然他的项目的第一次迭代使用 CAN 总线，但他搬到了日本，买了一辆没有 CAN 的旧斯巴鲁。新项目的工作类似于斯巴鲁选择监视器 v1 (SSM1)，但仍能很好地完成工作。

硬件使用华硕的修补板和 7 英寸屏幕的树莓 Pi，以及可以与 can(以及后来的 SSM1)接口的屏蔽。新的音乐是通过感应踏板位置来选择的，这使他能够更容易地触发他以前迭代的积极模式。这些都是用车速作为触发，这被证明是无效的产生预期的结果。当然，除了在你的车里打开音乐，你还可以用 can 总线做很多其他的事情。

 [https://www.youtube.com/embed/26vyWaAEJBI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/26vyWaAEJBI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

