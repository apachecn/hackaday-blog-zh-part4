# 定制终端中的 USB 铃声响起

> 原文：<https://hackaday.com/2020/09/13/usb-bell-rings-in-custom-terminal/>

旧的电传打字机甚至打字机都有铃声。真正的钟声。所以 ASCII 带字符应该发出真正的铃声。虽然一些现代终端从计算机扬声器发出嘟嘟声，但这是不一样的。[Tenderlove]肯定同意，因为他把一个微芯片 USB 转到 I2C 桥芯片变成了一个 HID 控制的铃铛。

我们看到的唯一问题是，你必须有一个到你的终端的补丁来响铃。我们希望看到一些 TCP 或串行过滤器，可以捕捉 BEL 字符，但从积极的一面来看，它很容易从任何类型的应用程序响铃，因为它响应正常的 HID 命令。

如果您对铃声不感兴趣，您可以使用相同的技术轻松地为任何东西添加数字输出。当然，你也可以根据需要使用 MCP2221A，并在那里放置一个带有数字 I/O 扩展器或任何数量的其他 I2C 芯片的 I2C 总线。

尽管视频的广告态度，你不能真的买这个铃铛。你必须做到这一点。只要相应地修改驱动软件，用 Arduino 或其他任何可以连接到 PC 的设备复制它并不困难。

我们知道你可以播放一个钟声的声音文件，但是有时候真的钟声是必要的。如果你想敲响警钟，原来有一个完整的[邪教想成为卡西莫多](https://hackaday.com/2016/12/02/quasimotor-a-robot-bell-ringer/)。

 [https://www.youtube.com/embed/uG8VpN6Z_YA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uG8VpN6Z_YA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

