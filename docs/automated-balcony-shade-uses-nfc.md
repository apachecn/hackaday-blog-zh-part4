# 自动阳台遮阳使用 NFC

> 原文：<https://hackaday.com/2021/01/20/automated-balcony-shade-uses-nfc/>

[Udi]住在一个带舒适阳台的公寓里。他还有三个孩子，现在大部分时间都在家，所以他发现自己在阳台上的时间比以前多了一点。为了提升他的体验，他安装了一个完全定制的遮阳控制器，随着时间的推移自动打开和关闭他的遮阳帘。

百叶窗和其他灯罩的自动马达可以买到，但是[Udi]的灯罩太大了，这些小马达都无法工作。找到一个 2:1 齿轮比的大型伺服系统是第一步，也是为它创建一个定制的安装到遮阳板上。一旦机械状况得到解决，他就编写了一个 ESP32 来控制伺服系统。ESP32 最初有控制按钮，但[Udi]最终过渡到 NFC，实现了限位开关功能，并为该版本实现了语音控制。

虽然不是我们见过的第一个 shade 控制器，但这个版本确实很好地利用了适当的硬件及其内置功能，尽管我们认为这可能是用 555 定时器完成的，但该项目进行得非常好，特别是对于[Ubi]的第一个 Arduino 兼容版本。但是，如果你决定复制这个建筑，如果需要的话，确保你的遮光板控制器是租赁友好型的。

 [https://www.youtube.com/embed/lLbN8Sc2E9Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lLbN8Sc2E9Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

