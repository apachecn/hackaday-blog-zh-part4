# 一个拉链头来结束你的变焦痛

> 原文：<https://hackaday.com/2020/12/28/a-pull-chain-to-end-your-zoom-pain/>

耶！另一个视频会议电话也在计划中，所以这肯定意味着是时候带着黯淡的笑容笨拙地摸索挂机键了。[【lane winfield】知道一定有更好的办法，并期待着拉链头开关的拯救](https://github.com/lanewinfield/zoomout)。当然，这可能只是一个按钮，但这有什么意思呢？此外，很少有按钮会像拉一条链来缩放呼叫那样令人满意。

拉链开关连接到模拟蓝牙键盘的 Adafruit Feather nRF52840 Express。固件方面，它发送命令+ F6，触发一个 AppleScript，手动退出，所有缩放调用和杀死指向 meet.google.com 的 Chrome 标签。他使用的是苹果的热键向导 Alfred，但这也可以用 AutoHotKey 之类的东西轻松处理。

拉链开关是小巧的机械装置。链条与一个凸轮相连，凸轮与一个轮子啮合，轮子的一半外侧有铜触点。当您拉动链条时，车轮移动 90 °,车轮触点与外壳内的固定触点连接起来，形成连接。再次拉动链条移动轮子，轮子滑动到没有触点的一半。看看下面的视频吧。

 [https://www.youtube.com/embed/x-K2vV-TWhk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/x-K2vV-TWhk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通路〔t0〕adafruit〔t1〕