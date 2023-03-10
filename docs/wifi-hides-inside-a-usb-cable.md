# WiFi 藏在 USB 电缆里

> 原文：<https://hackaday.com/2019/02/18/wifi-hides-inside-a-usb-cable/>

如果你以前不害怕 USB 线，现在你应该害怕了。来自[MG] [的 O.MG 线缆(或攻击性 MG 套件)在 USB 连接器](https://mg.lol/blog/omg-cable/)的外壳内隐藏了一个后门。把这根线插到你的电脑上，你就会成为无线网络远程攻击的受害者。

你可能会问，这种微小的 USB 电缆内部有什么使它容易受到这种攻击。这就是诀窍:在 USB“A”连接器的外壳内是一个加载了 WiFi 微控制器的 PCB 文件没有说明是哪一个——它将通过 USB 设备发送有效载荷。把它想象成一个 BadUSB 设备，就像 Hak5 的 [USB 橡皮鸭，但是你可以遥控它。这是进入系统的终极方式，任何人所要做的就是将一根随机的 USB 线插入他们的电脑。](https://shop.hak5.org/collections/physical-access/products/usb-rubber-ducky-deluxe)

在 bad USB——一个隐藏在设备 USB 控制器本身的漏洞——向世界发布的几年里，[MG]一直在不知疲倦地努力制造自己的恶意 USB 设备，现在它终于准备好了。O.MG 电缆在标准现成 USB 电缆的外壳内隐藏了一个后门。

这种设备的结构令人印象深刻，因为它完全适合 USB 插头。但这不仅仅是一个随机的中国纸板厂的 PCB:[MG]上个月花了 300 个小时和 4000 美元将这个项目与一家 Bantam 工厂组装在一起，[创造了他自己的 PCB，带有丝网印刷](https://twitter.com/_MG_/status/1090486321456414725)。不管怎么切都让人印象深刻。

这种电缆的未来更新将入侵任何计算机，可能包括一个端口 [ESPloitV2](https://github.com/exploitagency/ESPloitV2) ，这是一个开源的 WiFi 控制的 USB HID 键盘仿真器。这将给这个已经非常强大的设备带来巨大的能量。在这条推文所附的视频[中，你可以看到 O.MG 电缆连接到 MacBook 上，【MG】远程打开网页。](https://twitter.com/_MG_/status/1094389042685259776)