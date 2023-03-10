# Raspberry Pi 模拟真实的模拟电视体验

> 原文：<https://hackaday.com/2022/06/20/raspberry-pi-simulates-the-real-analog-tv-experience/>

如果你已经有了一台复古的模拟电视，有了修复 bug，并且你计划让最终项目至少在一定程度上符合时代，你会面临一个难题:你要看什么？当然，如今你可以提供任何数字内容，但有些节目在旧电视上播放感觉不太好。即使你有合适的复古节目，流媒体也不像我们在模拟时代那样，通过有些贫乏的选择来调整你的方式。

但是不要担心，这个树莓派电视模拟器可以让你的流媒体体验就像过去的模拟电视体验一样。它来自[Rodrigo],他发现了一台稍微被滥用的 5 英寸黑白便携式电视，正好适合改装。电视机下面的电池盒是安装 Pi 的最佳位置，它可以播放各种旧电影和短片。Arduino 读取原始调谐电位计的位置，告诉 Pi 您当前调谐到哪个“频道”。

复合视频从 Pi 的输出端直接输入到电视的视频输入端，图像质量就像你所期望的那样。但是对于我们的钱来说，真正卖这个的是使用一个继电器在频道转换之间的一小段时间内将电视调谐器切换回电路。这给了一个现实的静态和雪爆发，就像我们在过去的日子里忍受。向[罗德里戈]致敬，因为他捕捉到了过去电视中可怕的一切——确实是《迷失女人的台面》！—但仍然设法让它看起来不错。

 [https://www.youtube.com/embed/1pNfiL1X1ZA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1pNfiL1X1ZA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

