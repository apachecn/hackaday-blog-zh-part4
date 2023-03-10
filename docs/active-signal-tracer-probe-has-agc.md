# 主动信号跟踪探头有 AGC

> 原文：<https://hackaday.com/2022/06/24/active-signal-tracer-probe-has-agc/>

【电子新旧】有他一个老项目的新版本。最初的项目是一个积极的探索。他把他在建造探测器中学到的东西应用到新的探测器设计中。他还[增加了自动增益控制](https://www.youtube.com/watch?v=0c5ffSIuI-I)或 AGC。你可以在下面看到这个设计的视频解释。探头本质上是一个使用 JFET 的高阻抗输入，可以放大音频或解调的 RF 信号，这是在对无线电进行故障诊断时的一个方便设备。

音频放大器是一个简单的 LM386 电路。真正的工作是在输入级和新的 AGC 电路。老实说，我们已经将放大器本身用于类似的功能，尽管芯片的原始输入阻抗只有约 50K，在许多输入端使用电位计的电路中更低。拥有一个 JFET 缓冲器和一个 RF 解调二极管当然很方便。你会认为 AGC 模块会在音频阶段。不过，该设计将其放在检波器之前，只要放大器能够处理您感兴趣的 RF 频率，这就很好。在这种情况下，我们认为他主要是在旧的电子管 AM 收音机上工作，所以最大信号可能在 1 MHz 附近。

[![](img/c61be89016e65fb6ce74aae33e153c5b.png)](https://hackaday.com/wp-content/uploads/2022/06/sig2.png)

A similar device was a Radio Shack staple for many years

该模块利用具有 AGC 功能的 MAX9814 来放大驻极体麦克风。该模块有一个麦克风，这是为这个项目。数据手册没有提到频率上限，但类似的 Maxim 部分提到其增益在 600 kHz 时大于 5，因此对于这种可能使用的信号，它应该工作良好。我们想知道你是否可以使用该模块，并免除 JFET 输入。该芯片可能具有相当高的输入阻抗，但数据手册没有给出很好的说明。

多年来，我们一直使用 Radio Shack 的信号跟踪器，如果我们还能找到它的话，在几十年前原始电子设备出现故障后，现在它里面有一个 LM386。在那个时候，修理 AM 收音机需要使用这样的设备来找到你在哪里有和没有信号，或者在收音机的不同点注入信号。一枚硬币的两面。例如，如果您可以在音量控制上听到信号，这表明 RF 级是好的，而您在音频方面有问题。相反，如果你在音量控制上注入一个信号，听不到也意味着同样的事情。一旦你知道问题是在射频还是在房颤方面，你会把那部分大致分成两半，重复操作，直到你下降到一个坏的阶段。当然，你可以使用信号发生器和示波器，但在那个时代，你不太可能拥有它们。

当然，希斯基特有他们自己的版本。它甚至有一个神奇的[电眼管。](https://hackaday.com/2021/01/22/meet-the-magic-eye-vacuum-tube/)

 [https://www.youtube.com/embed/0c5ffSIuI-I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0c5ffSIuI-I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

