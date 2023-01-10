# 卡西欧手表获得 MEMS 振荡器升级

> 原文：<https://hackaday.com/2019/02/20/casio-watch-gets-a-mems-oscillator-upgrade/>

我们不得不承认自己有点像卡西欧 G-Shock 手表极客。这些又大又粗的手表每天都带着一些东西，这些东西经受住了我们分发的所有东西，直到智能手机让戴手表变得多余。但是其他人继续使用和滥用 G-Shocks，一些勇敢的灵魂甚至黑掉了它们。

用温度补偿 MEMS 振荡器取代标准石英晶体是[Alex]尝试过的一种方法，而且似乎效果不错。[他的项目报告](http://brainlubeonline.com/TCXOWatch/tcxoWatch.html)没有具体说明使用了哪种 MEMS 振荡器，但我们怀疑是 [SiT1552 TCXO](https://www.sitime.com/products/32-khz-tcxos/sit1552) 。凭借其极小的尺寸、在宽温度范围内的稳定性以及超低的功耗要求，该芯片是升级手表的 32.768 kHz 石英晶体的自然选择。问题是，1.5 毫米 x 0.8 毫米的微小芯片级封装(CSP)器件出现了一些处理问题。在回流焊炉中过度烹饪了一些芯片后，[Alex]能够将一个芯片安装到一个微小的分支板上，该分支板进入了之前由手表的石英晶体占据的空间。他从一个去耦电容器中为 TCXO 窃取了电力，将手表密封起来，它重新投入使用，稳定性更好，电池寿命更长。下面的视频显示了 TCXO 正在接受测试，旁边是原始的石英晶体和一个相对较大的 DS3231 RTC 模块，只是为了好玩。

[Alex]的 MEMS 移植似乎还有很长的路要走，而且为了边际收益要做很多繁琐的工作，但是我们有什么资格去评判呢？这确实让手表容易受到一点氦的撞击，这可能会让事情变得有趣。

 [https://www.youtube.com/embed/8hBEPXMFTcU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8hBEPXMFTcU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

