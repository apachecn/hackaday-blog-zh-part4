# 3D 打印蝶阀有助于自动排烟

> 原文：<https://hackaday.com/2021/02/09/3d-printed-butterfly-valve-helps-automate-fume-extraction/>

这不是我们经常想到的事情，但是在普通的车间里有大量的有害气体对人类健康有害。无论是焊接、激光切割还是 3D 打印，所有这些过程都会向空气中释放有害的化学物质，出于健康原因，最好将其过滤掉。为了帮助建立一个有效的过滤系统， [[Fab]需要一些阀门，所以他开始自己打印一些。](https://hackaday.io/project/177213-3d-printable-125mm-butterfly-valve)

[Fab]采用了简单的蝶阀设计，类似于大多数汽油动力汽车中的节流阀。蝶形叶片旋转以改变流量，由一个小 SG90 伺服转动。Wemos D1 迷你用于运行一对阀门，它们与 Y 形适配器配对，将焊接站和 3D 打印机连接到烟气抽取系统。作为一个很好的接触，一个支持 WiFi 的插座被连接到烙铁上，当它打开时，会通知 D1 迷你，打开阀门，自动开始排烟。

这是一个整洁的系统，将使[Fab]在未来的几年里在车间里轻松自如。[文件可用于那些希望为自己打印一套蝶阀的人。](https://github.com/Nerdiyde/NerDIYs_STLs/tree/main/STLs/butterfly_valve)[我们之前也见过其他智能油烟机。](https://hackaday.com/2019/08/07/workbench-fume-extractor-sucks-but-has-a-charming-personality/)休息后的视频。

 [https://www.youtube.com/embed/HIpqXohQ3vQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HIpqXohQ3vQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

