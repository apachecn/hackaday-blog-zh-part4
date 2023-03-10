# 代码评审灯巧妙地提醒你去帮助你的开发伙伴

> 原文：<https://hackaday.com/2018/11/01/code-review-lamp-subtly-reminds-you-to-help-your-fellow-developer/>

[Dimitris Platis]在一个接受代码变更的同行评审过程的环境中工作。代码审查通常是一件好事。然而，一个不利的方面是，缺乏来自其他开发人员的响应会导致团队的开发速度受到很大的影响。这并不是说其他开发人员不愿意做审查，而是因为个人经常专注于自己的工作，通知邮件很容易被忽略。这种情况也有一点“公地悲剧”的感觉，很容易感觉到有人*或*肯定会关注这种情况，但往往没有人这样做。为了解决这个问题，[Dimitris]建立了这个[代码审查灯](https://platis.solutions/blog/2018/09/26/code-review-lamp/)，一个微妙的通知，旨在促使审查者采取行动。

该灯是基于一个环的 RGB 发光二极管和一个 Wemos D1 迷你板。Wemos 采用流行的 ESP8266，因此易于开发。LED 环和 Wemos 通过一个光滑的定制 PCB 连接在一起。将 LED 环安装在 PCB 的顶部，将 Wemos 安装在底部，可以方便地通过 USB 电缆供电，同时将光线向上引导。该组件被放置在一个半透明的 3D 打印外壳中，产生令人愉快的漫射光源。

每个开发人员都有一盏代码审查灯。灯自动登录到变更管理系统，以检查是否有任何内容正在等待审查。如果审查准备就绪，灯会以特定于个人开发人员的颜色发光。所有这些都作为一个温和但持续的提醒，提醒人们某个人的工作正被搁置，直到评审完成。

我们喜欢这种设备有明确目的的方式:它在没有任何不必要的功能或部件的情况下完成工作。它与这个 [ESP8266 物联网运动传感器](https://hackaday.com/2018/07/19/a-super-simple-esp8266-iot-motion-sensor/)的相似之处在于，它只有一项工作要做，并且专注于它。

 [https://www.youtube.com/embed/TPO2nQkfprY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TPO2nQkfprY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

