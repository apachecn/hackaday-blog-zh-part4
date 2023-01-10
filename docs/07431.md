# 将蛇装进二维码

> 原文：<https://hackaday.com/2020/08/17/fitting-snake-into-a-qr-code/>

QR 码通常与 ASCII 文本相关联，如 URL 或序列号，但您知道您还可以将二进制数据编码到其中吗？为了展示这一概念，[MattKC]开始着手创建一个保存可执行版本 Snake 的[二维码。休息后的视频。](https://www.youtube.com/watch?v=ExwqNreocpg)

正如你所料，他最终使用的[版本 40 二维码](https://www.qrcode.com/en/about/version.html)比你通常看到的要大得多。它由 171×171 的网格组成，是大多数软件仍能读取的最大版本。这给了[MattKC]巨大的 2953 字节来处理。空间不大，但仍比过去的一些经典视频游戏要大。

首先，他使用 HTML、CSS 和 JavaScript 编写了 Snake 在 web 浏览器中运行，这能够适应可用的空间。现代浏览器用内置功能做了很多工作，而[MattKC]想要更多的挑战，所以他决定创建一个 Windows 可执行文件。他第一次尝试编译的 C 代码太大了，这导致了 x86 汇编的失败。在这里，他发现他的汇编知识太有限，如果不在项目上投入几个月的时间，就无法创建一个足够小的程序。他回到 C 语言，设法使用演示场景中常用的压缩链接器[压缩他的可执行文件。这将文件缩减到 1，478 字节。](https://github.com/runestubbe/Crinkler)

用于 Windows 的命令行条形码阅读器 Zbar 用于测试最终的 Snake 二维码。[MattKC]在 Zbarcam 中发现了一个错误，该错误阻止它通过网络摄像头输入读取二进制数据，因此通过开源的力量，他提交了一个错误修复程序，该程序现已集成到正式版本中。

任何人都可以在[【MattKC】的网站](https://itsmattkc.com/etc/snakeqr/)上玩所有的文件。下面的视频详细介绍了整个旅程。由于该项目证明软件可以嵌入二维码，这意味着如果智能手机二维码阅读器应用程序中的某个地方存在可利用的漏洞，恶意软件也可以隐藏在二维码中。

二维码是一个有趣的工具，有多种用途。深入了解[它们如何工作](https://hackaday.com/2018/11/05/a-qr-code-step-by-step/)，生成一个 [3D 打印版本](https://hackaday.com/2020/02/08/generate-3d-printable-qr-codes-with-this-web-tool/)，或者建造一个 [QR 点唱机](https://hackaday.com/2018/02/19/a-jukebox-for-the-21st-century-kit-blends-raspberry-pi-sonos-qr-codes/)，如果你想了解更多。

 [https://www.youtube.com/embed/ExwqNreocpg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ExwqNreocpg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

