# 删除主管密码并学习 Python

> 原文：<https://hackaday.com/2021/03/24/removing-supervisor-passwords-and-learning-python/>

当学习一门新的编程语言时，最好心中有一个目标，并朝着这个目标努力。[Timo]认为是时候学习 python 了，他心中也有一个项目:从他的旧 Thinkpad 中删除 BIOS supervisor 密码。从那以后，只需敲几下键盘(和一些焊接)，他就能从外部更改这个黑匣子的 BIOS 密码。

该构建利用一个 BeagleBone 通过 I2C 总线与笔记本电脑的 EEPROM 进行通信。当计算机不访问总线时，示波器也监视总线，每四秒钟寻找一个特定的窗口。在这段短暂的时间内，可以对 EEPROM 进行读写操作。窗口打开后，BeagleBone 会执行 Python 脚本，该脚本会尝试读取 EEPROM，还可以执行删除或更改 BIOS 管理程序密码等操作。

当然，在笔记本电脑上修改 EEPROM 有很高的破坏设备的风险，而且不是所有的笔记本电脑都使用相同的安全措施，甚至是这样的内存地址，所以文档和精度是关键。此外，对于这种老式的 Thinkpads，有可能用名为 libreboot 的自由/开源软件版本完全取代这些芯片上的固件，尽管这一过程很困难，但绝对值得推荐。

 [https://www.youtube.com/embed/slaXVUEYGh8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/slaXVUEYGh8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

