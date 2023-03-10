# 树莓派成为你需要的加密密码保管员

> 原文：<https://hackaday.com/2019/04/25/raspberry-pi-becomes-the-encrypted-password-keeper-you-need/>

除非你是一个到处使用相同密码的酷人，否则你可能需要一个硬件设备来保存你的用户名和密码。Passkeeper 是一个建立在 Raspberry Pi 上的硬件密码存储系统。它会加密你的密码，只有通过特殊密钥卡的魔力，你才能从这个设备中获取你的密码。

该设备的硬件是围绕 Raspberry Pi Zero 构建的。您可能会质疑 Pi Zero 的用途，但是考虑到它是一个完整的 Linux 系统，只需要几美元，它就有意义了。其余的硬件是一个微型有机发光二极管 SPI 显示器，一个 RFID 读卡器，几个发光二极管，一些电线和一些焊料。3D 打印的外壳将所有东西放在一起。

当然，这种构建完全是关于软件的，为此，Passkeeper 设备内置于 Go 中，具有一个构建 web 界面、构建固件并将所有内容写入 SD 卡的系统。使用时，只需将 Passkeeper 插入计算机的 USB 端口，它就可以作为网络接口出现。一切都可以通过 ping 一个 IP 地址，然后网络用户界面会记录你的用户名和密码。所有这些数据都是加密的，只有在 RFID 密钥卡存在的情况下才能解锁。这是一个有趣的想法，而且相当便宜。它不像 Mooltipass 那样完美，但是如果你身边有一个 Pi 并且没有密码管理员，这是这个周末要做的事情。