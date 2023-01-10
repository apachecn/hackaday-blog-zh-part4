# 使用良好的 USB 构建您自己的双因素认证器

> 原文：<https://hackaday.com/2022/06/18/build-your-own-two-factor-authenticator-with-good-usb/>

双因素身份验证正在成为许多应用程序和服务的标准，围绕电话移植黑客的安全问题正在导致基于 SMS 的系统逐步淘汰。在这种背景下， [[Josh]开发了他自己的认证设备，名为 Good USB。](http://optimumunknown.com/goodusb.html)

该设备可以使用 Arduino Leonardo、SS Micro 甚至 BadUSB 设备来构建。这是[乔希]最喜欢的后者，因为这个邪恶的设备被重新用于好的方面，所以它被命名为好 USB。基本上任何基于 Atmega32U4 的设备都可以工作，因为关键的功能是能够将 USB 键盘模拟到主机上。

使用该设备也同样简单。插入好的 USB 后，只需点击配套应用程序中的一个按钮，就可以为你登录的给定帐户生成一个代码。按下设备上的按钮，然后为您输入代码。或者，如果你的设备没有按钮，它可以设置为在你在配套应用程序中选择帐户后两秒钟内输入代码。

代码在 Github 上，供那些希望自己制作的人使用。谨慎者注意:这仍是一项进行中的工作，目前的实现可能存在安全漏洞。

如果你对 2FA 如何工作的细节感兴趣，我们已经详细研究过了。休息后的视频。

 [https://www.youtube.com/embed/6b-HfaJbiQg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6b-HfaJbiQg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

