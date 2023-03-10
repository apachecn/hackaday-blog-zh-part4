# 窃听助手扰乱寂静之声

> 原文：<https://hackaday.com/2020/03/22/eavesdropping-assistant-disturbs-the-sound-of-silence/>

除非你碰巧来自芬兰，否则这只是一个再熟悉不过的情况:你被困在一个不可避免的情况中，这个人与其说是朋友，不如说是熟人，你们两个都不知道谁应该说点什么，希望对话继续下去。尴尬的沉默是不可避免的，持续的时间越长，张嘴的想法就变得越痛苦。好吧，想想那些日子，感谢[Jasper Choi]和他的朋友们，他们给我们带来了解决尴尬沉默的[系统和互动增强器 T3，或 SASSIE。](https://www.instructables.com/id/SASSIE-the-System-for-Awkward-Silence-Solution-and/)

SASSIE 是一个激光切割的旋转圆柱体，配备了一对麦克风，可以检测并计算房间内任何持续沉默的持续时间。一旦达到预定义的时间限制，它会自动旋转到一个随机的方向，象征性地用手指指着房间里的一个人，指示现在该轮到他们发言了。为了打破沉默，手指的指向伴随着一些预先录制的信息。不幸的是，音频文件超出了这里使用的 Arduino Uno 的存储空间，所以责任必须在两个 Arduino 之间划分，并借助一些简单的串行通信进行安排。

虽然这显然是一个开玩笑的项目，但对于社交焦虑的人来说，这可能只是一个可喜的缓解，而且肯定有进一步发展这一想法的潜力。也许从这个快乐的机器人家伙那里得到一些灵感，未来的版本可能会通过提出一个话题来进一步缓和对话。

 [https://www.youtube.com/embed/Y9cKHJU2yeM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y9cKHJU2yeM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

