# 微型瘦客户机虽小但兼容

> 原文：<https://hackaday.com/2022/10/13/tiny-thin-client-is-small-but-compatible/>

我们对[moono nuration]的[微型瘦客户机项目](https://www.instructables.com/Arduino-Thin-Client/)印象深刻。它声称使用 Arduino，但正如你可能猜到的那样，它使用 Arduino 软件和支持网络的微控制器，如 ESP32。令人印象深刻的是，它符合标准并实现了 VNC 的 RFB 协议。

Arduino 上 [RFB 的原始代码来自【Links2004】，有了它，瘦客户端可能比你想象的更容易创建。然而，这个项目想使用更大的屏幕，发现这导致了某些问题。特别是，原始代码有一个 320×240 的显示器。该项目将使用 800×480 的显示器，但由于 ESP32 的限制，帧速率可能会低于每秒 7 帧。答案是将 16 位并行接口与更好的压缩结合起来返回到 VNC 服务器。](https://github.com/Links2004/arduinoVNC)

小键盘大概不是很实用，但是小巧。这将是另一个容易修改的东西。目前，键盘使用 I2C，但这将是直截了当的事情。这将是一个有价值的基础上建立一个更大的项目。3D 打印的外壳也不错。

我们已经看到了许多围绕商业瘦客户机构建的项目。一些停业的企业也是不知名零件的很好的 T2 来源。

 [https://www.youtube.com/embed/pTQ0KxgDNCE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pTQ0KxgDNCE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

