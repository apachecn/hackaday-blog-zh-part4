# 树莓派阅读它所看到的，让孩子们开心

> 原文：<https://hackaday.com/2021/10/31/raspberry-pi-reads-what-it-sees-delights-children/>

[Geyes30]的 Raspberry Pi 项目做了一件事:[它在相机的视野中找到任意文本，并大声读出它](https://theamateurengineersg.wordpress.com/2021/09/02/automated-reader-reading-printed-text-out-loud/)。它做得完美无缺吗？不完全是。组装起来至少不费力吧？也不是，但它很好地说明了将不同的功能粘合在一起创造新东西的过程。而且，[geyes30]的孩子们觉得它很吸引人，这本身就是一个胜利。

该设备由 Raspberry Pi 和相机制成，其工作原理是将相机中的静态图像发送到光学字符识别(OCR)程序，该程序将图像中的任何可见文本转换为 ASCII 表示。然后，识别出的文本通过管道传输到 [espeak](http://espeak.sourceforge.net/) 引擎，并大声朗读出来。让所有的工具都很好地发挥作用需要一些工作，但是[geyes30]很好地记录了一切，即使是新手也应该能够在一个下午就让项目启动并运行起来。

有时像文本到语音这样的功能本身就是最终结果。另一个类似的项目也是如此:[魔镜，其目的是不知疲倦地满足孩子们对语言的好奇心](https://hackaday.com/2018/05/27/magic-mirror-tirelessly-indulges-childrens-curiousity/)。

看到其他项目变得栩栩如生，学习新工具是获得新想法的好方法，记录它们有助于创意类型之间的交叉授粉。最近有什么事情激励了你，或者你已经记录了你自己的项目？我们想知道，其他人也想知道，所以[请通过提示热线](https://hackaday.com/submit-a-tip/)告诉我们！

 [https://www.youtube.com/embed/1bQYX0X5oF4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1bQYX0X5oF4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

