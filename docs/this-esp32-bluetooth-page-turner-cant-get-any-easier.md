# 这款 ESP32 蓝牙翻页器再简单不过了

> 原文：<https://hackaday.com/2021/05/27/this-esp32-bluetooth-page-turner-cant-get-any-easier/>

商业蓝牙踏板，旨在让音乐家在平板电脑上翻页，有一种你会想到的利基电子设备的虚高价格。[【joon as Pihlajamaa】决定用一个 ESP32 和一个便宜的脚踏开关来制作他自己的极低成本版本](https://codeandlife.com/2021/05/23/diy-bluetooth-sheet-music-page-turn-pedal-with-esp32/)，而不是为免手动翻页的特权支付高达 100 美元。

在硬件方面，没有比这更容易的了。所有[Joonas]需要做的就是将踏板连接到 ESP32 的一个数字引脚上，并将微控制器插入 USB 电源组。从那里，它变成了一个软件项目。有了*ESP32-BLE-键盘*库，只需要几行代码就可以根据踏板是被快速轻敲还是被按住一点来发送`RIGHT_ARROW`或`LEFT_ARROW`；允许他只需一个按钮就可以在页面间来回导航。

[Joonas]提到他使用的 ESP32 开发板太大，无法放入踏板本身，尽管我们想知道裸露的模块是否可以放在那里的某个地方。当然，你总是可以[用一点额外的空间](https://hackaday.com/2013/02/26/simple-to-build-programmable-foot-switches/)来安装电子设备，但在全球速卖通上不到 2 美元，这种交钥匙装置很难出错。

寻找替代方法？上个月我们报道了一款蓝牙翻页机,它将输入增加了一倍，并将其全部装入一个漂亮的木质外壳中。

 [https://www.youtube.com/embed/2suQec_JmzQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2suQec_JmzQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

