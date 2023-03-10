# 通过 ESP32 发送信号消息

> 原文：<https://hackaday.com/2021/07/05/messaging-on-signal-via-the-esp32/>

Signal 是一款流行的加密消息应用，通常用于智能手机。然而，由于[Dharmik]和[Tirth]的工作，跨平台服务现在可以通过 ESP32 使用。

演示很简单，使用配有两个按钮的 ESP32 微控制器。当一个按钮被按下时，它增加一个计数器，并发送一个信号信息记录当前计数。另一个按钮发送图像作为信号信息。

该项目依靠一个信号机器人来交付一个 API 密钥，使项目能够工作。通过使用这个密钥向 CallMeBot.com 服务器发出 HTTP 请求来发送消息。使用 API 密钥作为身份验证，用户只能向自己的号码发送消息，使系统免受垃圾邮件发送者的攻击。

虽然演示是基本的，但它只是用来说明项目是如何工作的。目的是让家庭自动化和其他物联网系统发送信号信息，通过这种方法，现在已经成为可能。高度安全意识的人可能不想依赖随机的第三方服务器，但对于那些瞎折腾的人来说，这可能没什么大不了的。

物联网有着悠久的自我信息项目历史；我们早在 2008 年就推出了推特烤面包机。休息后的视频。

 [https://www.youtube.com/embed/iFWuLX_fZZw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iFWuLX_fZZw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

