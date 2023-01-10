# 来自 MacGyver 文件:使用步进电机作为编码器

> 原文：<https://hackaday.com/2020/04/08/from-the-macgyver-files-using-a-stepper-motor-as-an-encoder/>

不难想象这样一个场景:你整天困在家里无事可做，某些物品供应短缺。当然，卫生纸得到了所有媒体的关注，但是试着买一些面粉或冰箱，看看你能走多远。此外，网上购物在此期间已经放弃了次日送达。一点也不难想象。现在假设你最新的自我隔离项目需要一个旋转轴编码器。如果没有，你会怎么做？如果你是技术型的，你可以在一台旧打印机上使用所有机器，并拉出一个步进电机。

步进电机如何变成编码器？好吧，这就是麦吉弗的部分。我们不太喜欢物理电路图，但看起来[Tech Build]借鉴了[一篇更早的文章](https://www.instructables.com/id/Using-Stepper-Motor-As-Rotary-Encoder/)，而且那篇文章有一个合适的原理图。

查看[Andriyf1]的原理图，你可以看到每个线圈都连接到一个运算放大器，作为正反馈比较器。结果应该是来自噪声输入的相当干净的方波。真正的诀窍是如何连接线圈，这取决于步进器如何布线。如果你有一个来历不明的步进电机，拿起你的欧姆表[阅读如何整理电线](https://hackaday.com/2011/12/01/an-introduction-to-stepper-motors/)。

最初的版本是在试验板上，但最终的是在原型板上。当然，Arduino 会读取脉冲。我们喜欢把东西用于意想不到的目的。扬声器和麦克风通常可以互换。发电机和马达也是。然后是[回形针](https://hackaday.com/2017/02/23/macgyvering-test-lead-clips/)。

 [https://www.youtube.com/embed/YhS-Sx-2is4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YhS-Sx-2is4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

