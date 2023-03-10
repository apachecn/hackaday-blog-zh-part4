# 使用这款 20 世纪 70 年代风格的桌面通知程序，永远不会错过任何一封电子邮件

> 原文：<https://hackaday.com/2022/07/05/never-miss-an-email-with-this-1970s-style-desktop-notifier/>

如果你喜欢 20 世纪 70 年代的审美，但认为喇叭裤、大头发和迷幻壁纸在这个时代有点太多了，你可能想看看[【Pierre Muth】](https://pierremuth.wordpress.com/2022/07/03/the-absurd-notifier/)*的最新作品。这是一个有用的桌面配件，为你的办公室增添了一点 70 年代的风格:在一个看起来像橙色电视的闪亮金属脚上，有一个小工具可以告诉你是否有重要的电子邮件等待或约会即将到来。*

 *[Pierre]围绕一个 Garmin Vivosmart 3 智能手表建立了这个系统，他买的很便宜，因为它的显示屏坏了。显示器的引脚和协议当然没有记录，所以[Pierre]连接了他的逻辑分析仪，试图弄清楚它是如何工作的。原来这是一个简单的 SPI 设置，经过一点点尝试和错误，他能够提取手表发出的图像。

为了更换破碎的屏幕，[Pierre]转向一些 128×64 像素的 VFD 显示器，这是他在早期项目中留下的。它们的分辨率与 Garmin 的原始有机发光二极管显示器完全相同，但它们的接口不同:VFD 预期 115k2 串行数据。对一端为 SPI 端口、另一端为 UART 端口的 PIC 微控制器进行编程，可以在两者之间建立简单的桥接。

[Pierre]然后设计并 3D 打印了一个让人想起 20 世纪 70 年代电视的外壳，并配有亮橙色。最终的结果是一个时髦的小复古时钟，在复古的绿色显示屏上显示通知。如果你喜欢桌面通知程序，我们看到了几个简洁的通知程序，提醒它们的主人从 YouTube 新用户到国际空间站经过 T2 的事情。

 [https://www.youtube.com/embed/p4yUZXCd6N4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p4yUZXCd6N4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[阿德里安]！*