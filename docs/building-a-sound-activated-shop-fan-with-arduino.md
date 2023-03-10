# 用 Arduino 构建一个声音激活的商店风扇

> 原文：<https://hackaday.com/2020/02/10/building-a-sound-activated-shop-fan-with-arduino/>

无论你用的是烙铁还是台锯，店里的通风都很重要。这就是为什么[原子乳品]建造了一个名为 Fanboy 的巨型空气净化器，它看起来应该安装在 F-15 的机翼下。意识到墙上的一个简单开关无法实现这一强大的空气推进器正义，[他们决定为它建造一个声音激活控制器](https://www.youtube.com/watch?v=keLmohaZByE)。

[![](img/dac9f20199d6b4a3b10d135ec8e7f7ae.png)](https://hackaday.com/wp-content/uploads/2020/01/soundfan_detail.jpg) 这当然是一个优雅的想法。即使是最简单的声音探测硬件也很难忽略他们敲击木工工具时发出的声音。在最基本的层面上，他们所需要的是一旦房间中的噪音水平达到特定的阈值，Arduino 就会抛出一个继电器。

当然，它最终会变得比这更复杂，这是这类项目中容易发生的事情。首先，声音不会直接控制风扇控制器中使用的固态继电器。当配备了麦克风的 Arduino 检测到足够的噪音时，它会启动一个计时器，让风扇运行两个小时。如果工具继续运行，那么更多的时间将被添加到时钟中。这可确保室内空气流通良好，即使在切割和打磨完成后。

[原子乳品]还增加了一些额外的功能，这样他们可以更直接地控制风扇。有一个按钮可以手动增加时间，另一个按钮可以关闭时间。甚至还支持一个小小的无线遥控器，因此风扇可以在不走到控制面板的情况下操作。

这些年来，我们已经看到了一些令人印象深刻的空气循环和灰尘收集系统，但是考虑到在任何给定的时间都可能使用大量的工具，找到一种优雅地打开和关闭它们的方法一直是一个问题。声音激活并不是一个完美的解决方案，但它肯定是我们为自己的商店考虑的一个方案。

 [https://www.youtube.com/embed/keLmohaZByE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/keLmohaZByE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

