# DIY Streamdeck 帮助你使你的 Twitch 表演专业化

> 原文：<https://hackaday.com/2022/11/12/diy-streamdeck-helps-you-professionalize-your-twitch-show/>

Twitch 上的专业人士和业余爱好者的唯一区别是产品价值。这一切都是为了平稳过渡，你永远也不会发现那些大牌在中途摆弄那些不可靠的软件。实现这一点的关键是通过一个 streamdeck 来帮助控制你的设置，[就像来自[electronio OBS]的这个简单的设计。](https://www.youtube.com/watch?v=Mjs67IEtZYY)(视频，下面嵌入。)

该构建依赖于 Arduino Micro，这是一个微控制器板，完全可以充当 USB 宏键盘。它配有一个 Nextion LCD 触摸屏，显示各种流控制功能的按钮，如显示“马上回来”屏幕或播放视频剪辑。该版本还具有更大的常规按钮，用于重要的快速访问功能，如静音麦克风。这一切都被包裹在一个 3D 打印的外壳中，一些可寻址的 RGB LEDs 通过另一个 Arduino 来添加一些活力。巧妙之处在于，构建发送 F13-F24 的键码，这允许 streamdeck 的热键避免与任何其他使用传统键盘热键的软件冲突。

这是一个有用的工具，对 Twitch 或其他平台上的任何人都有用。或者，[你可以重新利用一部旧手机做类似的工作](https://hackaday.com/2022/07/18/quick-hack-the-phone-to-stream-deck-conversion/)。休息后的视频。

 [https://www.youtube.com/embed/Mjs67IEtZYY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Mjs67IEtZYY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

