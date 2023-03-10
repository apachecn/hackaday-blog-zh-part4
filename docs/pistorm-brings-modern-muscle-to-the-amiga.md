# PiStorm 为 Amiga 带来了现代肌肉

> 原文：<https://hackaday.com/2021/04/19/pistorm-brings-modern-muscle-to-the-amiga/>

众所周知，Amiga 是有史以来设计得最好、最伟大的计算机，但它仍然是一个过时的平台。它的 68K 和后来的 PowerPC 架构都被主流抛弃了，它吸引人的灰色工业设计也不再是商店货架上的亮点。然而，这并不意味着这个平台已经死了，像克劳德·施瓦茨这样的铁杆粉碎者正努力通过像 PiStorm 这样的项目来保持它的活力。

PiStorm 是一个摩托罗拉 68K CPU 仿真器，运行在 Raspberry PI 3A 上。Pi 使用其 GPIOs 与 CPLD 芯片交互，CPLD 芯片充当逻辑粘合剂，允许现代单板计算机仿真 Amiga 的原始处理器。然而，这不仅仅是更换或升级 CPU 的简单方法。它还提供了额外的功能，如可重定目标的图形加速，SCSI 磁盘仿真，以及运行任何你想要的 Kickstart 的能力。

虽然最初的工作是在 Pi 3A 上完成的， [[Claude]也展示了在 Pi CM4 上运行的一些基本功能](https://mobile.twitter.com/Claude1079/status/1383669659648495625)。基准比碧昂斯超级碗中场秀更激烈，所以如果你需要在你的经典 Amiga 上咕哝，这可能是一条路要走。另外，在 Github，[上可以很容易地获得构建你自己的文件，这应该使它比其他 Amiga 加速器板更容易访问。](https://github.com/captain-amygdala/pistorm)

我们想知道这个加速器是否可以用来将 Amiga 连接到 Spotify，就像之前的版本一样。有可能，时间会证明一切。休息后的视频。

> 展示最新 PiStorm 68k 仿真的小视频。所有这些都在 A500+ (ECS，1MB 芯片)上运行，只需插入 PiStorm 和一个保存 HDF 硬盘映像的 USB 硬盘。CPU 设置为 68EC030，RTG 720 p/16 bit，128MB Fastmem。[#阿米加](https://twitter.com/hashtag/Amiga?src=hash&ref_src=twsrc%5Etfw)#拉斯贝里比 https://t.co/giTjdoiG4wpic.twitter.com/HsPu47JrnT
> 
> —克劳德·施瓦茨(@ Claude 1079)[2021 年 2 月 19 日](https://twitter.com/Claude1079/status/1362840304999661568?ref_src=twsrc%5Etfw)