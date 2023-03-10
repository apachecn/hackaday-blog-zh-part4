# 这到底是什么东西？

> 原文：<https://hackaday.com/2018/10/21/what-the-hack-is-this-thing/>

让我们玩一个猜谜游戏。这里展示的是专为今年 11 月 2 日至 4 日在帕萨迪纳举行的 [Hackaday 超级大会](https://www.eventbrite.com/e/hackaday-superconference-2018-tickets-47386813234?aff=1021com)打造的硬件演示的后视图。当完成时，它肯定会让一群人高兴，但是如果你和我们一样，研究像这样一个项目的完成面背后的东西甚至比看到最终产品更令人满意。

如果你认为你知道它是什么，你可以从会议中获得一个免费的[硬件徽章！请在下面留下您对这是什么的最佳猜测，我们将选出最有可能赢得徽章的人。](https://hackaday.com/2018/10/17/the-supercon-badge-is-a-freakin-computer/)

想仔细看看吗？[点击此处嵌入](https://hackaday.com/wp-content/uploads/2018/10/back-on-2.jpg)。

## **更新:**我们有一个赢家！

Zardam 很快就意识到这是《2001:太空漫游》中 Hal 9000 电脑控制台的复制品。恭喜你。

 [![HAL1](img/d71aeb0e345c675445d798d3cfa2bc67.png "HAL1")](https://hackaday.com/2018/10/21/what-the-hack-is-this-thing/hal1/)  [![lens back 2](img/3e3b51f8d039efb1fc71d80cc97de654.png "lens back 2")](https://hackaday.com/2018/10/21/what-the-hack-is-this-thing/lens-back-2/)  [![back on 2](img/91d075ce83f5ebd10242fc7a1d78a4e6.png "back on 2")](https://hackaday.com/2018/10/21/what-the-hack-is-this-thing/back-on-2/) 

### Voja Antonic 对该版本的一些评论:

> The red circular plate at the bottom is a PIR motion sensor, which is a part of another project and has nothing to do with HAL or badge. There is a clearly visible 915 MHz module, which is disconnected and has no function in this project.
> 
> It is connected to the raspberry in the lower left corner, just because it has to provide about 3V voltage, and it uses the LDO of raspberry. It also generates reset signals for all four RAPIs, because as a result, the 5V power supply (lower right corner) provides a slowly rising voltage when turned on, so RAPIs will not start up at all without external reset.
> 
> When someone walks up to Hal, the motion sensor will randomly trigger one of Hal's 30 sentences in the movie. That's why the raspberry in the lower left corner is connected to the amplifier, and there is an extra line from the motion sensor board to GPIO 24\.

### 演示视频:

 [https://www.youtube.com/embed/44kpwE2Mv1I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/44kpwE2Mv1I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 猜对的奖励:

[![](img/2fae31b8e2a0446050ca528dc2486559.png)](https://hackaday.com/wp-content/uploads/2018/10/2018-supercon-badge-featured.jpg)

Voja Antonics 制造漂亮的硬件。Hackaday 超级会议徽章是一件艺术品，就像 Hal 9000 控制台一样。Voja 将和其他数百名优秀的黑客一起出现在 Supercon。来和我们一起度过一个难忘的周末吧！