# 跳恐龙变成了一种真正的锻炼

> 原文：<https://hackaday.com/2020/04/06/offline-dinosaur-jumping-becomes-a-real-workout/>

很高兴看到人们在当前的危机中努力寻找有趣的锻炼方式。虽然跳上跳下对膝盖不好，但它确实能给人不错的有氧运动。但是如果你没有绳子或水坑，我们承认跳跃会很快失去弹力。

对[星期五]来说，隔离是一段充满游戏的时间。在几款 FPS 游戏之间，[他决定尝试玩谷歌离线的基于恐龙的侧滚游戏，每当他身体跳到空中时，就让恐龙跳过仙人掌](https://www.youtube.com/watch?v=Jtt03-zsEIM)。(视频，嵌在下面。)

它的工作原理是这样的:[frid ay]拥有一个发射电路，该电路由一个 Arduino UNO、一个加速度计模块和一个 nRF24L01 收发器组成，所有这些都使用 9 V 电池运行。每当[Friday]跳跃的时候，加速度计就会读取 Z 的变化，并发送给接收电路，接收电路不过是另一个 UNO 和 nRF。接收 UNO 连接到笔记本电脑，并配置为按下空格键，以便恐龙在仙人掌上慢跑。

我们从来没有能够在游戏中存活足够长的时间来看到这种情况发生，但显然你需要在游戏中的某个时刻蹲下。[Friday]还没有对此实施控制，但我们确信他会想出办法的。跳过休息时间去看视频，如果你需要密码，就打电话给他。

如果你有很多零件，为什么不做一个实体版本呢？

 [https://www.youtube.com/embed/Jtt03-zsEIM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Jtt03-zsEIM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通过 [r/duino](https://www.reddit.com/r/arduino/comments/fuwrwj/i_created_a_controller_for_google_dinosaur_game_i/)