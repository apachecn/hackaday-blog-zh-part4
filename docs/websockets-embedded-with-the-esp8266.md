# 嵌入 ESP8266 的 WebSockets

> 原文：<https://hackaday.com/2018/10/03/websockets-embedded-with-the-esp8266/>

以前是网页浏览简单。您向服务器请求一些文本，这些文本被及时发送，然后由您的浏览器格式化。现在，网页很可能是一个完整的应用程序，可以阅读邮件、编辑文本或许多其他内容，并可以使用 WebSockets 创建一个到服务器的反向通道。由于像 ESP8266 这样的廉价硬件，现代网络浏览器可以做的事情之一就是感知和控制现实世界。[Acrobotic]有一个关于使用 WebSockets 让浏览器实时与 ESP8266 网络服务器对话的有趣视频。你可以在下面的视频中看到他的简单演示。

当然，您将使用您在 ESP8266 上使用的常用语言— [Acrobotic]在 Arduino IDE 中使用 C++。在浏览器端，您将使用 JavaScript，尽管它将被嵌入到作为 web 服务器的 C++程序中。

同样要记住的是，还有其他几种方法可以做到这一点。例如，您可以请求不同的 URL，或者在查询字符串中传递数据。这里的问题是性能会受到影响，因为每次都必须建立新的连接。你想和服务器交易。您也可以使用 AJAX 方法，但是它们效率也不高，因为它们主要是为了动态更新网页的一部分。web socket 非常简单，正如你在视频中看到的，性能非常好。它还方便了使用相同服务的非基于浏览器的客户端。

我们已经看到这种技术被用来驾驶四轴飞行器。WebSockets 已经存在一段时间了，所以你的浏览器应该支持它们。如果不行，你可以随时使用[这一招](https://hackaday.com/2013/02/07/gifsockets-websockets-using-animated-gif-files/)——至少在一个方向上。

 [https://www.youtube.com/embed/ROeT-gyYZfw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ROeT-gyYZfw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

