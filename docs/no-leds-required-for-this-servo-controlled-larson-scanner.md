# 这个伺服控制的拉森扫描仪不需要发光二极管

> 原文：<https://hackaday.com/2022/02/13/no-leds-required-for-this-servo-controlled-larson-scanner/>

总的来说，很容易让一个 LED 灯条依次点亮，并让它来回跳动。把这个简单的动画变成一个真正的拉森扫描仪，有平滑的过渡和受控的淡出，完全是另一回事。完全忘记发光二极管，让[成为一个伺服操作的拉森扫描仪](http://www.riderx.info/larson-scanner-servo-edition/)是——好吧，让我们称之为硬件抽象中有趣的一课。

拉森扫描仪以著名电视制片人[格伦·A·拉尔森](https://hackaday.com/2014/11/17/larson-scanner-namesake-glen-larson-passes-away/)的名字命名，因为他喜欢将它融入像*太空堡垒卡拉狄加*和*霹雳游侠*这样的节目中，实际上很难在硬件上执行，因为当它在显示器上来回跳舞时，它的尾巴会随着领先像素的消失而消失。[Eric Gunnerson]决定用 [Fade](https://hackaday.com/blog/?s=fade-an-esp32-animation-system) 让这个和其他动画效果更容易实现，这是一个在 ESP32 上运行的 LED 动画定制框架。

LED 动画很好，但伺服呢？可以修改 Fade 来支持它们吗？由于 Fade 的架构和[Eric]通过 PWM 信号对不可寻址 led 的现有支持，这被证明是一个相当容易的 mod。通过添加 UDP 连接，将多个 ESP32s 置于中央微控制器的控制之下，ESP32s 甚至可以支持 16 个以上的 PWM 通道。

下面的视频展示了[Eric]的伺服支持演示，带有一个八通道机电 Larson 扫描仪。每个“像素”都是一个在业余爱好伺服系统上来回摆动的彩色乒乓球，整个事情听起来就像你想象的那样糟糕。如果你斜视得恰到好处，效果看起来很有说服力，但这不是重点。这里真正的故事是[Eric]深思熟虑的架构，这使得 mods 比从头开始更容易。

 [https://www.youtube.com/embed/6Fb6g7Kf85k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6Fb6g7Kf85k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

