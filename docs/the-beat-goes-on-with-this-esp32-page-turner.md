# 节拍随着这款 ESP32 翻页机继续

> 原文：<https://hackaday.com/2021/04/16/the-beat-goes-on-with-this-esp32-page-turner/>

寻找一种免提方式在 iPad 上翻阅乐谱，[【The _ 落叶松】基于 ESP32](https://www.reddit.com/r/esp32/comments/mniscy/esp32_bluetooth_page_turner_the_enclosure_is_made/) 设计出了这款简单的蓝牙输入设备。微控制器只需要将两个开关连接到 GPIO 引脚，在这种情况下，您可以在吉他踏板上找到相同的重型柱塞，以及 USB 隔板直通来提供电源。多亏了优秀的`ESP32-BLE-Keyboard`库，当按下左键或右键时，只需要几行代码就能触发相应的按键。

[![](img/546452010484d97a892d668a7196e4b3.png)](https://hackaday.com/wp-content/uploads/2021/04/esp32turner_detail.jpg) 不可否认，从电子学的角度来看，这是一个简单的项目，但与我们通常在这些地方看到的 3D 打印产品相比,[ The _ 落叶松]建造的木质外壳是一个有趣的转变。它起源于从一张旧餐桌上回收的橡木条，它们被层压在一起形成一个固体块。然后用一个大铲钻在石块上钻孔，为电子设备留出一个空间，第二块橡木平板被制成前面板。

使用 ESP32 创建蓝牙输入设备是如此简单，以至于我们真的有点惊讶，我们没有看到更常用的技巧。尤其是当你[考虑到所有定制键盘](https://hackaday.com/2020/09/21/custom-keyboard-goes-split-gets-thin-acquires-stained-wood/)在过去几年[给这些页面增光添彩](https://hackaday.com/2020/09/07/40-keyboard-build-is-100-open-source/)。任何想要的人都可以得到这些工具，所以你不得不怀疑黑客们是不是不喜欢将蓝牙用于像键盘这样重要的东西？