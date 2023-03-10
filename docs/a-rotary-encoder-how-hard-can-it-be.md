# 旋转编码器:能有多难？

> 原文：<https://hackaday.com/2022/04/20/a-rotary-encoder-how-hard-can-it-be/>

你[可能已经注意到](https://hackaday.com/2022/04/13/arming-with-an-os/)，我[一直在使用 Mbed](https://hackaday.com/2022/04/19/arm-pumps-up-the-volume-with-mbed-and-a-potentiometer/) 与 STM32 ARM CPU 一起工作。Mbed 曾经非常简单，但自从它演变成 Mbed OS 以来，已经发生了很大的变化。不幸的是，这意味着你能找到的许多库和例子不能在新的系统上工作。

我需要一个旋转编码器——我从你看到的“Arduino 的 49 块电路板”套件中拿出一个便宜的。我敢肯定，这不是世界上最好的编码器，但应该够用了。不幸的是，Mbed OS 没有编码器的驱动程序，我发现的前几个第三方库要么通过轮询工作，要么无法与最新的 Mbed 一起编译。当然，读取编码器并不是一个神秘的过程。自己写代码能有多难？确实有多难。我想我会分享我的代码和我如何到达那里的过程。

有许多方法可以读取旋转编码器。有些可能比我的方法更好。还有，这些廉价的机械编码器很可怕。如果你想做精密的工作，你可能应该考虑一种不同的技术，比如光学编码器。我提到这一点是因为几乎不可能完美无缺地阅读其中任何一篇。

所以我的目标很简单:我想要中断驱动的东西。我发现的大多数都需要你定期调用一些函数或者设置一个定时器中断。然后他们建立了一个状态机来跟踪编码器。这很好，但是这意味着即使编码器不动，你也要消耗大量的处理器来检查编码器。STM32 的 CPU 可以很容易地中断一个引脚的变化，所以这就是我想要的。

## 问题是

当然，问题是机械开关会反弹。所以你必须用硬件或软件来过滤这种反弹。除了电容器之外，我真的不想加入任何额外的硬件，所以软件必须处理它。

我也不想使用任何非绝对必要的中断。Mbed 系统使得处理中断变得容易，但是有一点延迟。实际上，在这一切结束后，我测量了延迟，并没有那么糟糕——我稍后会谈到这一点。不管怎样，我决定只使用一对中断。

## 理论上

理论上，读取编码器是小菜一碟。有两个输出，我们称之为 A 和 b。当你转动旋钮时，这些输出发出脉冲。内部的机械排列是这样的，当旋钮向一个方向转动时，来自 A 的脉冲比来自 b 的脉冲超前 90 度，如果你向另一个方向转动，相位就会反过来。

![](img/333547efa955655fb27a1b5e9c563279.png)

人们通常认为脉冲是正向的，但大多数实际编码器都有一个接地触点和一个上拉电阻，因此实际上，当什么都没发生时，输出通常为高电平，而脉冲实际上为低电平。你可以在图中看到，当没有人转动旋钮时，有一个很长的高信号。

注意在图的左侧，B 信号每次都在 A 信号之前下降。如果你在 A 的下降沿对 B 进行采样，在这种情况下你将总是得到 0。当然，脉冲的宽度取决于你转动的速度。当你转向另一个方向时，你会看到图的右边。这里，A 信号首先变为低电平。如果你在同一点采样，B 现在是 1。

请注意，A、B 或顺时针和逆时针标签没有什么神奇之处。它真正的意思是“一条路”和“另一条路”如果你不喜欢编码器的移动方式，你可以交换 A 和 B 或者在软件中交换。我只是随意选择了那些方向。通常，通道 A 应该以顺时针方向“引导”，但它也取决于您测量的边缘以及您如何连接所有东西。在软件中，你通常在一个方向的计数上加 1，在另一个方向上减 1，以了解你在一段时间内的位置。

有很多方法可以解读这种输入。如果您正在对它进行采样，那么从这两位构建一个状态机并以这种方式处理它是相当容易的。输出形成一个格雷码，因此您可以丢弃不良状态和不良状态转换。然而，如果你对你的输入信号有把握，事情会简单得多。只需在 A 的一边读 B(反之亦然)。如果你想要更强的鲁棒性，你可以验证另一边。

## 在实践中

不幸的是，真正的机械编码器看起来不像上面的图表。它们看起来更像这样:

 [![A better drawing](img/342c3490e37102406e2adc0ea7fcbff7.png "Created with GIMP")](https://hackaday.com/created-with-gimp-15/) A better drawing [![Actual scope trace](img/3e22802f753040e4d0e2ffbec56c1e5b.png "IMAGE2")](https://hackaday.com/2022/04/20/a-rotary-encoder-how-hard-can-it-be/image2-17/) Actual scope trace

这就导致了一个问题。如果您在输入 A 的两个边沿(示波器上的上部轨迹)中断，您将在两个边沿获得一系列脉冲。请注意，B 在 A 的每个边沿处于不同的状态，所以如果你总共得到偶数个脉冲，你的总计数将为零。如果你幸运的话，你可能会在正确的方向得到一个奇数。否则你可能会走错方向。真是一团糟。

但是在 A 的采样边缘，B 坚如磐石。示波器下面的轨迹看起来像一条直线，因为所有的 B 过渡在那个比例下都不在屏幕上。这就是让编码器轻松去抖的秘密。当 A 在变化时，B 是稳定的，反之亦然。由于它是格雷码，这是有道理的，但正是这种洞察力使简单的解码器成为可能。

## 这个计划

所以计划是注意 A 何时从高变低，然后读取 B，然后忽略 A，直到 B 改变。如果你想监控 B，当然，它也有同样的问题，所以你必须锁定它到 A，它在变化时是稳定的。在我的例子中，我不想再使用两个中断，所以我遵循这个逻辑:

1.  当 A 下降时，记录 B 的状态并更新计数。然后设置一个锁定标志
2.  如果 A 再次下跌，如果设置了锁定标志或者 B 没有改变，则什么也不做。
3.  当 A 上升时，如果 B 已经改变，记录 B 的状态并清除锁定标志。

这意味着在上面的范围轨迹中，顶部轨迹的第一次下降导致我们读取 B。之后，屏幕上的任何过渡都不会有任何影响，因为 B 没有改变。在 B 经历了高噪声的高电平到低电平转换之后，屏幕上出现的上升沿将会解锁算法。

## 问题是

不过，有一个问题。整个方案基于这样的想法，即 B 在 A 的真正上升沿与下降沿相比是不同的。有一种情况，B 不变，但我们仍然想接受 A 的优势。那就是你改变方向的时候。如果你监视 B，这很容易解决，但是这需要更多的代码和两个中断。相反，我认为，对于一个拧旋钮的人来说，如果你非常快速地朝不同的方向疯狂地拧，你甚至不会注意到编码器的一两下咔哒声走错了方向。你会注意到的是，如果你做一个微调，然后故意扭向另一边。

![](img/77e5258c16e47c4b4ee51bfdfb7a2f36.png)

当你认为你知道 B 的先前状态，而在一段时间内(比如几百毫秒)什么都没有改变时，代码会将其 B 的想法重置为未知，这样无论如何下一个 B 信号都将被认为是有效的。

我使用了 Mbed 的`Kernel::Clock::now`特性。不清楚你是否应该从中断服务程序(ISR)中调用它，但是我是这样做的，而且它似乎工作起来没有问题。

唯一的另一个问题是确保在读取过程中计数不会改变。我禁用了读取周围的中断只是为了确保。

## 代码

你可以在 [GitHub](https://github.com/wd5gnr/MbedQuadratureEncoder) 上找到代码。如果你理解了所有的解释，你理解起来应该没有问题。

```

void Encoder::isrRisingA()
{
   int b=BPin; // read B
   if (lock && lastB==b) return; // not time to unlock
// if lock=0 and _lastB==b these two lines do nothing
// but if lock is 1 and/or _lastB!=b then one of them does something
   lock=0;
   lastB=b;
   locktime=Kernel::Clock::now()+locktime0; // even if not locked, timeout the lastB
}

// The falling edge is where we do the count
// Note that if you pause a bit, the lock will expire because otherwise
// we have to monitor B also to know if a change in direction occurred
// It is tempting to try to mutually lock/unlock the ISRs, but in real life
// the edges are followed by a bunch of bounce edges while B is stable
// B will change while A is stable
// So unless you want to also watch B against A, you have to make some
// compromise and this works well enough in practice
void Encoder::isrFallingA()
{
   int b;
   // clear lock if timedout and in either case forget lastB if we haven't seen an edge in a long time
   if (locktime<Kernel::Clock::now())
     {
     lock=0;
     lastB=2; // impossible value so we must read this event
     }
   if (lock) return; // we are locked so done
   b=BPin; // read B
   if (b==lastB) return; // no change in B
   lock=1; // don't read the upcoming bounces
   locktime=Kernel::Clock::now()+locktime0; // set up timeout for lock
   lastB=b; // remember where B is now
   accum+=(b?-1:1); // finally, do the count!
}

```

由于有了`InterruptIn`类，设置中断很容易。这就像一个`DigitalIn`对象，但是有一种方法将一个函数附加到上升或下降沿。在这种情况下，我们两者都用。

## 潜伏

我想知道在这个设置中处理一个中断需要多少时间，所以如果你设置了`#define TEST_LATENCY 1`，代码是可用的。你可以看到我的结果的视频，但是 TLDR:得到一个中断不超过 10 微秒，通常是一半。

 [https://www.youtube.com/embed/MKwPSaQiNO8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MKwPSaQiNO8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



获得正确的编码器比我想象的要难一点，但主要是因为我不想处理更多的中断。修改代码来观察相对于 A 引脚的 B 引脚，并真正了解 B 的正确状态，这很简单。如果您尝试修改代码，这里有另一个想法:通过测量中断之间的时间，您还可以了解编码器的转动速度，这对某些应用可能很有用。

如果你想重温格雷码以及它的一些有用之处，我们之前已经讨论过了。如果这一切听起来很熟悉，我[在 2017 年在旧版本的 Mbed](https://hackaday.com/2017/01/11/encoders-spin-us-right-round/) 上使用了编码器。在这种情况下，我使用了一个固定的库，它定期轮询定时器中断的输入。但就像我说的，总有不止一种方法让这种事情发生。

【头条图片: [SparkFunElectronics 的](https://www.flickr.com/photos/41898857@N04)[旋转编码器](https://www.flickr.com/photos/41898857@N04/15659597894)，2.0 的 CC。太棒了。]