# TinyPilot 提供 KVM-over-IP，成本低，延迟更低

> 原文：<https://hackaday.com/2020/07/24/tinypilot-provides-kvm-over-ip-with-low-cost-and-even-lower-latency/>

远程访问很棒，但是如果机器停止启动，停止连接网络，或者需要像 BIOS 设置或启动管理这样的低级交互，远程访问就没有价值了，因为它只有在主机启动并运行时才可用。通常的解决方案是将键盘和显示器拖到有问题的机器上进行物理访问。

[![](img/72ed273a7b7e3c1ebf09a3a9457309e8.png)](https://hackaday.com/wp-content/uploads/2020/07/tinyPilot-Featured.jpg)

Ubuntu laptop (right) being accessed over IP, via web browser on the left.

对于大多数人来说，以这种方式交换电缆充其量是一项不常见的任务。但是对于那些更接近于管理硬件或开发软件的人来说，将键盘和显示器插入或拔出机器的需要会令人厌倦。现代的解决方案是基于 IP 的 KVM(键盘、视频、鼠标),但是商业选择是昂贵的。另一方面，迈克尔·林奇的 TinyPilot 的零件价格约为 100 美元，包括一个树莓 Pi 和 USB HDMI 捕捉设备。它必须从 KVM 中去掉“M ”(这意味着它还不支持鼠标),但它的其余部分都是通过网络浏览器完成的。

TinyPilot 到底是做什么的？它通过网络浏览器提供远程访问，但该设备是一个独立的硬件，从主机的角度来看，它与物理键盘和显示器没有什么不同。这意味着键盘和视频访问在主机启动之前就可以工作，所以即使改变 BIOS 设置也没有问题。

[Michael]在下面嵌入的视频中演示了他的设计，但我们鼓励您[查看项目页面](https://mtlynch.io/tinypilot/)以了解 TinyPilot 开发过程中所有挑战的精彩探索。

 [https://www.youtube.com/embed/IF-AyHJ8DOI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IF-AyHJ8DOI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感兴趣吗？自己做一个，或者作为一种选择[Michael]已经准备了一个工具箱。TinyPilot 没有提供主机电源开关的接口，但如果你需要添加，你可以使用[另一个 KVM 项目的](https://hackaday.com/2017/11/05/twin-pis-for-remote-computer-management/)方法，将继电器模块与你自己的一些 DIY 集成在一起。