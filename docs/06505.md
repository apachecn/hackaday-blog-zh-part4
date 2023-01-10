# 打开激光激射器外壳，可以产生更大的效果

> 原文：<https://hackaday.com/2020/05/08/open-laser-blaster-shells-out-more-bang-for-the-buck/>

[a-RN-au-D]想和他的儿子一起做些有趣的事情，于是想出了一个激光爆破游戏，这应该会让他参加年度父亲的竞选。它原本只是用纸板做的，但你知道这些东西是怎么回事。我们很高兴设计进行到这一步，因为那个爆破器看起来棒极了。

blaster 和 target 都运行在 Arduino Nanos 上。blaster 中有一个 5mW 的激光模块，还有一个扬声器，用于播放您选择的 pew pew 相关的声音。按下爆炸按钮，激光击中安装在目标中间的光敏电阻。当目标被击中时，它在 9g 伺服系统上向后摆动，然后迅速返回垂直位置进行下一次射击。

有一些不太明显的功能，真正使这款游戏一炮而红。blaster 可以在 10 人射击模式(或 6 人，或你在代码中更改的任何模式)下运行，具有内置的重新加载延迟，或可以设置为全自动。如果你空间不足或者厌倦了将目标移动到不同的平面上，它可以安装在墙上——目标在被击中时向前移动，然后重置为平面。休息之后，请查看我们上传的演示视频。

没有打印机？没问题— [这里有一个 Node-RED 射击场，使用简单的木制靶子](https://hackaday.com/2020/01/14/node-red-laser-shooting-gallery-goes-anywhere/)。

 [https://www.youtube.com/embed/QoEO9-xC1Es?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QoEO9-xC1Es?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

