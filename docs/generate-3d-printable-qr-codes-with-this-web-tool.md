# 使用此网络工具生成 3D 可打印二维码

> 原文：<https://hackaday.com/2020/02/08/generate-3d-printable-qr-codes-with-this-web-tool/>

由于如今大多数人口袋里都装着一台带摄像头的电脑，二维码可以成为一种很好的方式来轻松分享简短的信息片段。您可以将它放在您的名片上，以便人们可以快速访问您的联系信息，或者用您网络的 SSID 和加密密钥放在您客厅的墙上。二维码的设计也使它们非常适合 3D 打印，由于一种新的基于网络的工具，[你可以在几秒钟内生成你自己的定制 STL](https://flxn.de/qrcode2stl/)。

该网站由[Felix Stein]创建，为二维码的许多可能选项提供了一个易于使用的界面。显然，您可以完全控制代码的实际内容，无论是简单的 URL 还是更具体的内容，如预先格式化的 SMS 消息。但是你也可以调整物理参数，比如尺寸和厚度。

一旦你对 3D 预览满意了，你可以让网站为单个或多个挤压打印机生成一个 STL。对于我们这些使用单一挤压机的人来说，你需要手动改变适当层的细丝颜色。由于涉及到如此多的变量，您还需要自己找出应该在哪个层进行交换。

顺便说一句，这是 STL 不尽如人意的一个很好的例子。当使用像 3MF 这样的格式时，颜色和材质信息可以直接嵌入到模型中。一旦在一个足够现代的切片机中打开，所有棘手的部分都会自动分类。或者至少，[这是 Prusa Research 对](https://hackaday.com/2019/11/01/josef-prusa-wants-you-to-change-file-formats/)的期望。