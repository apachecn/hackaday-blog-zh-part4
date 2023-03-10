# 按钮，按钮，谁有(一个)按钮？

> 原文：<https://hackaday.com/2018/12/17/button-button-whos-got-the-one-button/>

我们经常认为少即是多，但是你能用一个只有一个按钮的设备做什么呢？[Danko berto VI]也想知道同样的事情，他制作了一个只有一个按钮和一个显示屏的 Arduino。在做了一些显而易见的事情(如计数器或秒表)后，他决定为他最新的 *Volos 项目*视频制作一个计算器。

你可以在网上找到[源代码](https://www.youtube.com/redirect?v=LhFTZ7ekLEE&redir_token=6u_zP5zyspS6RuX2EByWSQ2cXNh8MTU0NDgzMDA1N0AxNTQ0NzQzNjU3&event=video_description&q=https%3A%2F%2Fdrive.google.com%2Fopen%3Fid%3D15eqhB3Uoax9whUirtt5j_O8AblLskoxJ)，他使用[GitHub](https://github.com/mathertel/OneButton)的一个库来处理对单次按压、两次按压和长时间按压的反应。理想吗？大概不会。但是，如果你只有有限的空间或引脚，它可以使一个可行的项目和一个你不能完成的区别。

他最初的项目还包括克隆一只拍打鸟。有机发光二极管显示器只有 64×48，所以空间并不大。微型 Arduino 的包装、电池和显示器都放在一个好看的盒子里，令人印象深刻。所以这个装置可能有所用途。

当然，这个库可以和任何程序一起工作，没有理由你不能有一个以上的按钮，简单地用相同的策略增加它们的功能。GitHub 上有一个例子，展示了如何创建两个连接到不同硬件设备的 OneButton 对象。

对了，小盒子可能只有一个按钮，但也有电源开关。事实证明，在某些情况下，你可以将它用作[输入。如果有机发光二极管的展示让你觉得过于奢华，试试](https://hackaday.com/2016/11/18/only-one-button-no-problem/)[双星](https://hackaday.com/2016/10/08/minimal-operating-system-one-button-one-led/)。

 [https://www.youtube.com/embed/LhFTZ7ekLEE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LhFTZ7ekLEE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

