# 附加组件使 ESP32 摄像机板更容易编程

> 原文：<https://hackaday.com/2020/01/09/add-on-board-makes-esp32-camera-board-easier-to-program/>

当开发板有一些令人讨厌的小怪癖，使它们比应该的更难使用时，你难道不讨厌吗？以 2019 年初开始在市场上出现的 ESP32-CAM 为例。理论上，这个东西很神奇:一个支持摄像头和 SD 卡的 ESP32，所有这些都不到 10 美元。问题是编程可能有点痛苦，需要额外的设备和多余的手指。

Bitluni 不是一个轻易接受这种挑战的人，他为 ESP32-CAM 开发了一个很好的编程板，你可能想看看。该问题源于 ESP32-CAM 上缺少 USB 端口。这一设计决定使得用户需要一个 USB 转串行适配器，该适配器必须连接到相机板的 GPIO 引脚，以便在按下复位按钮时可以从 Arduino IDE 上传程序。这些都不太复杂，但是很不方便。他的解决方案被称为 cam-prog，它不仅负责 USB 转换，还负责重置电路板。它通过简单地重启相机，允许草图通过 USB 上传来实现。这看起来是一个非常方便的板，将在[的 Tindie 商店](https://www.tindie.com/stores/bitluni/#store-section-products)出售。

为了演示这个插件，他编写了他的 ESP32-CAM 程序，并将其连接到他巨大的乒乓球视频墙上。视频质量大约是你对每像素 40 毫米的 1200 像素显示器的预期，但它仍然非常平滑——平滑到足以使他在视频最后几分钟的解释性舞蹈动作非常有趣。

 [https://www.youtube.com/embed/ikhZ34WgObc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ikhZ34WgObc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

