# 最简单的伪随机数发生器

> 原文：<https://hackaday.com/2019/04/23/the-simplest-of-pseudo-random-number-generators/>

一个真正的随机数是很难产生的。一种典型的方法是从自然和不可预测的来源，如放射性衰变或热噪声中产生所需的偶然因素。相比之下，生成看起来随机但实际上遵循可预测序列的数字是非常容易的。具有通过其输出和其中一个级的 XOR 的反馈的移位寄存器将产生在设定周期后重复的伪随机位的连续流。

[KK99]使用三位移位寄存器创建了最简单的伪随机二进制序列发生器。这是在一块令人愉快的复古 perfboard 上实现的，用 CD4047 作为时钟发生器，用 74HC164 移位寄存器来完成这项工作。不同寻常的是，XOR 门是由分立晶体管制成的，2N3053s 封装在庞大的 TO39 封装中，为了获得特别老式的外观，一个老式的惠普 LED 显示器显示当前生成的数字。结果是一个相对无用的周期为七位的伪随机序列，但这个电路的目的是教育而不是它的效用。你可以在下面的视频中看到它的运行。

早在 2016 年，我们就演示过使用伪随机序列的危险。被英国密码破译者昵称为“Tunny”的德国军用密码依赖于机械序列发生器，它被破解的故事导致了第一台存储程序电子计算机的发展 [Colossus。](https://hackaday.com/2016/08/23/colossus-face-to-face-with-the-first-electronic-computer/)

 [https://www.youtube.com/embed/3g2sKt6q3H8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3g2sKt6q3H8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)