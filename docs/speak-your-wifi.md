# 说出你的 WiFi

> 原文：<https://hackaday.com/2018/10/31/speak-your-wifi/>

当你为物联网创造一个东西的时候，你就制造了一台小电脑，它做一件简单的工作，可能有一个最小的界面。但是最小化的界面留给配置的空间很小，比如输入 WiFi 细节。也许如果你自己做的话，你已经在代码中硬编码了你的 WiFi 凭证，但是这很难转化为多个实例。那么，如何轻松地将最终用户 WiFi 凭据放在多个东西上呢？也许[Rob Dobson]用他的技术[找到了答案，他把它们作为一系列可听见的音调](https://www.youtube.com/watch?v=h2k5u4pWs-U)发送出去。

浏览器中有一段 Javascript 代码，你可以在其中输入你的 WiFi 凭据，然后通过扬声器表达为一组 FSK 音，由设备上的麦克风采集。然后它们可以被解码成凭证，这个东西就可以连接了。所有的代码都可以在 GitHub 上找到，如果你喜欢的话。

当然，这不是什么新鲜事，任何一个拥有带盒式接口的 8 位机器的人都会告诉你。从表面上看，它比那些笨拙的即兴热点要容易得多，它们有一个网络界面，你可以连接并传递你的凭证。但是，虽然我们很喜欢这种便利，但我们不禁想知道，在 audible free space 中表达凭证对许多读者来说是否有点太不安全了。然而，这项技术仍然有效，我们确信可能会找到其他不太敏感的应用程序。与此同时，我们希望他没有在休息时间下面的视频中无意中分享他的 WiFi 密码。

 [https://www.youtube.com/embed/h2k5u4pWs-U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/h2k5u4pWs-U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

