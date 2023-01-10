# 通过机器学习和皮卡丘避免重复性劳损

> 原文：<https://hackaday.com/2022/03/04/avoid-repetitive-strain-injury-with-machine-learning-and-pikachu/>

自从 1984 年苹果麦金塔电脑普及以来，不起眼的鼠标已经成为桌面计算体验的重要组成部分。虽然鼠标实现了用户友好的图形用户界面，从而使更多的人比以往任何时候都可以使用计算机，但它们也导致了重复性劳损(RSI)的显著增加。主要由不良姿势和压力引起的 RSI 会导致手和手臂的疼痛、麻木和刺痛感，用户可能只会在太晚的时候注意到这些。

kutluhan_aktar 希望在 RSI 出现之前捕捉到它的迹象，他发明了一种设备来跟踪老鼠的疲劳情况。它通过两个传感器来实现:一个测量皮肤电反应(GSR)，另一个执行肌电图(EMG)。这两个测量值合在一起，应该给出肌肉酸痛量的指示。传感器读出电路连接到 Wio 端子，这是一个带 2.4 英寸 LCD 的小型 ARM Cortex-M4 开发板。

但是，计算肌肉酸痛并不是简单的把几个数字加在一起；事实上，传感器数据和肌肉健康状态之间的联系足够复杂，以至于[kutluhan]决定训练一个 TensorFlow 人工神经网络(ANN)，考虑到在现实生活中收集的观察到的压力水平。当他使用鼠标时，网络在 Wio 上运行，按下按钮来指示他经历的压力量。经过几轮训练后，他最终建立了一个准确率超过 80%的网络。

[kutluhan]还设计了一个相当整洁的 3D 打印外壳，用于容纳传感器读出板以及为 Wio 终端供电的电池。很自然地，这个案例被 3D 再现的皮卡丘所增色不少(明白吗？一个可以麻痹对手的鼠标神奇宝贝！).在他早期的[胖丁二氧化碳传感器](https://hackaday.com/2021/11/16/jigglypuff-sensor-breathes-co2-so-you-dont-have-to/)中，我们已经看到了【库特鲁汉】对神奇宝贝主题项目的喜爱。

虽然多传感器的设置对于日常使用来说似乎不太实用，但鼠标疲劳估计器可能是一个有用的工具，可以训练自己在使用鼠标时保持良好的姿势并避免压力。如果你也用键盘(谁不用呢？)，确保[你也正确地使用它](https://hackaday.com/2021/07/22/avoiding-repetitive-stress-injury-invest-in-yourself-now-or-pay-later/)。

 [https://www.youtube.com/embed/p9jePOv4epg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p9jePOv4epg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

