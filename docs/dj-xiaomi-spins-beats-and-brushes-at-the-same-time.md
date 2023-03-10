# DJ 小米同时旋转节拍和画笔

> 原文：<https://hackaday.com/2019/09/13/dj-xiaomi-spins-beats-and-brushes-at-the-same-time/>

[Eddie Zhang]的这篇博客文章直接来自“只因我能”部门，它向我们展示了让小米机器人吸尘器充当可能是世界上最不必要的 Spotify Connect 扬声器是多么容易。你的家会成为 DJ 小米即兴表演的下一个东道主吗？从休息后的视频中演示的音频质量来看，我们对此表示怀疑。但是这个技巧确实让我们对真空黑客的现状有了一个有趣的了解。

在这个黑客的第一阶段，[Eddie]利用了 [Dustcloud](https://github.com/dgiese/dustcloud) ，这是一个正在进行的项目，用于记录和逆向工程各种小米智能家居设备。使用这里提供的信息，您可以获得对您的真空吸尘器的根级 SSH 访问，并安装您自己的软件。有一句话你从没想过会读到，对吧？

有了 vacuum rooted 之后，[Eddie]就会安装一个 Spotify Connect 客户端，用于 Raspberry Pi。由于它们都是 ARM 设备，该软件在小米机器人上运行得足够好，但 Linux 环境需要稍微调整。也就是说，您需要手动创建一个新贵。conf 文件，因为 vacuum 没有安装 systemd。又出现了一个意想不到的句子。

我们当然对机器人真空黑客并不陌生，尽管历史上 iRobot Roomba 一直是这种恶作剧的目标平台。其他玩家进入这个领域对我们这些看到家用电器被推出舒适区之外而感到兴奋的人来说只能意味着好事。

 [https://www.youtube.com/embed/qwqWNIM_aY8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qwqWNIM_aY8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 Ohmohm 的提示。]