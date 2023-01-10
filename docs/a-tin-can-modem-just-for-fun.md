# 一个锡罐调制解调器，只是为了好玩

> 原文：<https://hackaday.com/2020/07/18/a-tin-can-modem-just-for-fun/>

任何一个年龄足够大的人都可以愉快地回忆起调制解调器通过电话线进行连接时发出的“哔哔声-哔哔声-嘎嘎声”序列，可能还记得简单的“锡罐电话”实验，其中一根绷紧的绳子将声音振动从一个锡罐底部传递到另一个锡罐底部。这个锡罐调制解调器实验将这两种体验放在一个项目中。

正如[Mike Kohn]所指出的，这个项目比看起来要困难得多。实际上，他在优化项目的锡罐电话部分时比在整理电子产品时要困难得多，结果他尝试了很多东西，从标准的锡罐到纸质咖啡杯，最终确定了一对硬纸板坚果罐，金属底的那种。用一段风筝线连接在一起——牙线不起作用——[迈克]在一端加了一个发射器，另一端加了一个接收器。

发射机使用 ATtiny 2313 和大家最喜欢的音频放大器[lm 386](https://hackaday.com/2016/12/07/you-can-have-my-lm386s-when-you-pry-them-from-my-cold-dead-hands/)，而接收机则配备了驻极体麦克风前置放大器板、LM566 音频解码器和 MSP430 微控制器。调制方案尽可能简单——一个 400 Hz 的音调，其长度随 1 或 0、停止或开始位而变化。连接到一对终端程序上，[迈克]能够通过~~线~~串发送他的名字，他计算的是 6 或 7 波特。

这个项目具有锁定无聊的所有特征，但我们不在乎，因为它很有趣，也是一个很好的学习机会，特别是对年轻人来说。还有大量的优化空间——也许它甚至可以快得足以应付黑客时代的复古 300 波特挑战。

 [https://www.youtube.com/embed/myWLHgp6dkw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/myWLHgp6dkw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

