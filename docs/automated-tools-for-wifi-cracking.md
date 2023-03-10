# WiFi 破解的自动化工具

> 原文：<https://hackaday.com/2020/09/30/automated-tools-for-wifi-cracking/>

了解 WiFi 网络如何被攻击是正确保护它们的一个重要部分，了解它的最好方法是(合法地)进行一些攻击。[Matt Agius]已经进入了 WiFi 破解的兔子洞，并在这个过程中创建了 [Pwnagotchi 工具](https://github.com/mtagius/pwnagotchi-tools)来自动化实际的密码破解部分。

破解 WiFi 网络的第一步是记录客户端连接到接入点时交换的握手。多亏了 [Pwnagotchi](https://hackaday.com/2019/10/16/a-tamagotchi-for-wifi-cracking/) ，这变得非常简单，它将一个 Raspberry Pi 变成了一个自动化的握手收集工具，Pwnagothi 工具有助于自动化接下来的步骤。它从 pwnagotchi 下载握手(pcap 文件)，并将其转换为 pmkid/hccapx 文件，以便与 [hashcat](https://hashcat.net/hashcat/) 密码恢复工具一起使用。然后可以使用[Matt]编译的任何攻击为实际破解生成 Hashcat 脚本。WPA/WPA2 破解速度慢，需要大量的处理能力，因此[Matt]还增加了自动供应 AWS GPU 实例的选项，以便在云端运行破解任务。它还记录每个被破解的握手的状态。

随着无线网络和物联网设备变得越来越普及，了解危险以及如何防范它们非常重要。WiFi 和蓝牙安全可能是最容易了解的，但当使用 [RTL-SDR](https://hackaday.com/2019/07/31/rtl-sdr-seven-years-later/) 时，其他网络也同样容易受到攻击。另一个选择 [Flipper Zero](https://hackaday.com/2020/09/02/flipper-zero-blasts-past-funding-goal-and-into-our-hearts/) ，这是一个受 Pwnagotchi 启发的 1 GHz 以下网络黑客工具，最近在其 Kickstarter 活动中达到 480 万美元。