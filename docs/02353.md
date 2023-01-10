# ESP 平台的远程调试

> 原文：<https://hackaday.com/2019/03/07/remotedebug-for-esp-platforms/>

调试工具对于快速有效的开发至关重要。如果不能窥见真实情况，就很难理解和解决问题。那些生活在 Arduino 平台上的人可能很熟悉使用串行端口进行调试，但这远不是唯一的方法。【JoaoLopesF】已经为 ESP 平台编写了 [RemoteDebug](https://github.com/JoaoLopesF/RemoteDebug) 工具，结果令人印象深刻。

RemoteDebug 完全取消了串行接口，而是使用 ESP 的本地无线接口通过 TCP/IP 发送调试数据。这一切都是通过 telnet 处理的，完全不受平台限制。通过 WiFi 连接处理事情，它消除了物理访问的问题，以及电缆和有限串行端口的麻烦。这对机器人项目也有好处，调试时不再需要系绳。

它有一套类似于[【joalopesf】早期作品 SerialDebug 的功能。](https://hackaday.com/2018/11/07/debugging-arduino-is-painful-this-can-help/)像冗长和时间戳这样的东西都是内置的，这样就可以很容易地获得高质量的调试数据，而不必自己重新发明轮子。休息后的视频。

 [https://www.youtube.com/embed/T4nxdsFUGgg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T4nxdsFUGgg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

