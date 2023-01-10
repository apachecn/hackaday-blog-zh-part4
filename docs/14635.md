# 使用 Pi Pico W 将屏幕共享到 RGB 面板

> 原文：<https://hackaday.com/2022/08/28/share-screen-to-rgb-panel-with-pi-pico-w/>

RGB LEDs 非常适合为你的生活增添一点色彩，使用它们的矩阵作为图形显示更令人满意。[bitluni]用 Pi Pico 构建了一个 RGB LED 显示屏，你可以在上面[分享你电脑屏幕的像素化版本](https://www.youtube.com/watch?v=yzRHAdS9FLY)。

[bitluni]希望在[rasbery Pi Pico W](https://hackaday.com/2022/06/30/raspberry-pi-pico-w-adds-wireless/)上获得一些使用 [MicroPython](https://hackaday.com/2021/04/29/wireless-micropython-programming-with-thonny/) 的经验，之前曾使用 WebSockets 通过 WiFi 传输显示数据。不幸的是，可用的 MicroPython WebSockets 实现没有为其余代码留下足够的 RAM。相反，他在 Pico 上设置了一个简单的 HTTP 服务器，以 POST 请求的形式接收像素数据。这使得刷新率较低，但仍然看起来很棒，特别是 3D 打印背投帧。

为了从电脑发送显示数据，[bitluni]使用一个简单的本地托管 HTML 页面，该页面接受 Pico 的 IP 地址，并提示您选择要共享的显示器或窗口。它使用 JavaScript 获取显示数据，生成所需的低分辨率像素值，并发送 POST 请求。

这看起来像是一个有趣的周末项目，可以添加到你的实验室或家里，而且只需要花费大约 20 美元。这基本上是他的[巨型乒乓球墙展示](https://hackaday.com/2019/08/29/giant-led-display-is-1200-balls-to-the-wall/)的缩小版。

 [https://www.youtube.com/embed/yzRHAdS9FLY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yzRHAdS9FLY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

