# ESP32 Hash Monster 用数据包填充口袋

> 原文：<https://hackaday.com/2020/09/08/esp32-hash-monster-fills-pockets-with-packets/>

除非你是在大海中央或森林深处阅读这篇文章，否则很有可能你周围都是无线网络。捕获它们只需要有合适的硬件和软件，然后你就可以着手破解用来加密它们的密钥了。虽然这种事情显然有邪恶的含义，但审计该地区无线网络的强度肯定有合法的理由。

它本身可能没有破解任何加密的计算能力，但如果你安装由[G4lile0] 开发的哈希怪物固件[，ESP32 M5Stack 就可以胜任捕获 WiFi 数据包的任务。即使你不打算走得更远，这个项目也通过添加一些图表和动画角色(同名怪物本身)来寻找 WiFi 接入点并获取它们的数据包，这是一种迷人的转移，这些动画角色以空气中所有看不见的 1 和 0 为食。](https://github.com/G4lile0/ESP32-WiFi-Hash-Monster)

[有一些优秀的文档向您展示了在 Hash Monster 的帮助下打开 WiFi 网络的整个过程，但这仅仅是这个小工具的可能性的开始。快速搜索](https://telescope.ac/petazzoni/the-hash-monster-esp32-tamagotchi-for-wifi-cracking)[发现了许多软件项目](https://medium.com/@elkentaro/m5-stack-shitty-code-ssid-scanner-collector-3a1dd1eaf3c2)，它们利用了 M5Stack 相对于更传统的 ESP32 板的特定优势，即内置屏幕、按钮和电池。我们甚至在 Hackaday，[上看到它被用在一些构建中，比如这个 DIY 热感相机](https://hackaday.com/2018/06/08/who-said-thermal-cameras-werent-accessible-to-the-masses/)和[定制的舰载计算机系统](https://hackaday.com/2020/03/28/an-open-source-shipboard-computer-system/)。

【感谢曼纽尔的提示。]