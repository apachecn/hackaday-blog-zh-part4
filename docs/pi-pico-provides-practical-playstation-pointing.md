# Pi Pico 提供实用的 PlayStation 指点

> 原文：<https://hackaday.com/2022/07/12/pi-pico-provides-practical-playstation-pointing/>

我们现在还不清楚为什么最初的 PlayStation 需要一个鼠标(尽管我们确信有很多人急于在评论中告诉我们)，但是如果你想要给这个近 30 年的老游戏机增加改进的指向功能，[【沃伊奇·萨拉杰卡】的这个项目肯定是值得关注的](https://github.com/Franticware/usb-to-playstation-mouse)。

[![](img/444f8ba576fd44ef5b368f8073f7761c.png)](https://hackaday.com/wp-content/uploads/2022/07/psmouse_detail.jpg) 这个名副其实的“USB 转 PlayStation Mouse”项目确实如其名——将普通的 USB 鼠标改造成索尼经典游戏机的输入设备。将一个放在一起需要一个 Raspberry Pi Pico，一个带母 USB-A 连接器的 5 V DC-DC USB 升压模块，以及一个牺牲控制器或外设来提供电缆和专有连接器。

根据简单的接线图组装好硬件后，您只需将 Pico 插入您的计算机并复制固件文件。[vojt ch]指出，在尝试上传固件之前，您需要拔掉鼠标，这可能是因为两个 USB 端口上的数据引脚已经绑在一起了。

也不要担心必须找到一些晦涩的标题来试用你的新外设，[vojt ch]说，如果你在驱动器中没有光盘的情况下启动鼠标，它可以在系统的主菜单中工作。现在你只需要几张 [Raspberry Pi Pico PlayStation 存储卡](https://hackaday.com/2022/06/13/raspberry-pi-pico-replaces-playstation-memory-card/)就能完成整套。