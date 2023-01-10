# Pico 做 PID

> 原文：<https://hackaday.com/2022/01/13/pico-does-pid/>

比方说，如果你想控制一个温度，你可能会认为你可以打开加热器，直到你达到所需的温度，然后关闭加热器。这种方法是可行的，但不是最理想的——你可能会超过目标，然后随着系统冷却下来，你必须赶上，结果往往是系统在期望值附近振荡，但永远不会真正稳定在正确的温度上。为了解决这个问题，你可以使用 PID——比例积分微分——循环，这就是[veebch]用 [Rasberry Pi PICO](https://github.com/veebch/heat-o-matic) 和 Micropython 所做的。

想法是基于实际温度和期望温度之间的差异量(比例误差)来控制输出信号。此外，该金额根据长期误差(积分)和任何短期变化(导数)进行调整。下面你还可以看到一段视频，讲述如何使用控制回路制作更好的 *sous vide* 汉堡。

当然，PID 对于温度控制以外的事情也很有用。它们通常适用于任何(通常是线性的)控制值影响其他值的过程。例如，我们已经看到机器人使用 PID 来[跟随线](https://hackaday.com/2021/09/18/line-following-robot-uses-pid-for-speed/)。有些人也用它们来保持平衡，或者你可以用[来平衡一个球](https://hackaday.com/2019/07/31/ping-pong-ball-makes-great-pid-example/)。

 [https://www.youtube.com/embed/rooKTWVzXWw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rooKTWVzXWw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

