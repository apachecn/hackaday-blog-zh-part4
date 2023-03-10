# 激光笔和 Arduino 打造极简射击游戏

> 原文：<https://hackaday.com/2021/10/18/laser-pointer-and-arduino-make-a-minimalistic-shooting-game/>

视频游戏很棒，但有时你除了在屏幕上观看动作之外，还想要操纵实际物体的快感。这一定是任天堂的猎鸭游戏如此受欢迎的原因，尽管它的游戏简单。多产的黑客[mircemk]类似地制作了一款名为“[激光射击游戏](https://hackaday.io/project/182210-diy-arduino-laser-pointer-shooting-game)”的计算机加实体游戏，不知何故让我们想起了古老的 NES 游戏。

该游戏基于 Arduino Nano，连接了五个 led 和五个光敏电阻(ldr)。当游戏开始时，发光二极管随机亮起，玩家有有限的时间用激光笔“射击”相应的 LDR。这个时间限制随着游戏的进行而减少，一旦玩家没有按时击中目标，游戏就结束了。“游戏结束”的信息伴随着悲伤的曲调，但幸运的是没有咯咯笑的狗。

完整的图表和代码可供任何人尝试复制或改进这个游戏。不，你不能简单地一直用你的激光扫过五个 ldr，因为如果你射错了目标，你就输了。更多基于激光笔的游戏，试试这个[激光命令克隆](https://hackaday.com/2010/05/04/laser-command-game-uses-laser-for-control/)或者这个[激光标记徽章系统](https://hackaday.com/2020/02/13/star-wars-themed-laser-badge-all-that-is-missing-is-the-pew-pew-sound-effect/)。

 [https://www.youtube.com/embed/txJJOOVtNQE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/txJJOOVtNQE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

