# 给橡子电子加 WiFi

> 原文：<https://hackaday.com/2020/09/25/adding-wifi-to-the-acorn-electron/>

在无数爱好者不断寻求让每一台 80 年代的 8 位家用电脑体验不涉及 9600 波特调制解调器的在线体验的乐趣时，[Roland Leurs]为 Acorn Electron 创造了一个基于盒式磁带的模块，增加了 WiFi，他在 2020 年 9 月的虚拟 ABug 会议上向[展示了这一模块。](http://abug.org.uk/index.php/2020/09/05/wifi-on-the-acorn-electron-roland-leurs/)

橡子电子是一台基于 Synertek 6502 的计算机，于 1983 年 8 月在英国发布。这是著名的 BBC 微型教育/家用电脑的预算版本，有 32 kB 的内存，其 ROM 中有 BBC BASIC v2。[Roland]的 ElkWiFi 卡插入一个可用的盒式插槽中，之后可以启用板载 ESP8266 (ESP-1 模块)并将其用作 WiFi 调制解调器。

[![](img/b20f739d0f080b88f6006339be8818ab.png)](https://hackaday.com/wp-content/uploads/2020/09/acorn_electron_wifi_setup.jpg)

Acorn Electron with Plus 1 expansion, ElkWiFi and additional expansion card inserted.

该板采用 Exar [ST16C2552CJ](https://pdf1.alldatasheet.com/datasheet-pdf/view/85178/EXAR/ST16C2552CJ.html) 双 UART 芯片，其中一个通道连接到 ESP-1 模块，另一个通道用作非专用 UART 接头。控制逻辑用 VHDL 实现并闪存到板载 Xilinx CPLD，128 kB RAM 模块用作 WiFi 数据缓冲区。

虽然这是一个明确的利基产品，但阅读论坛帖子会让人真正体会到技术的复杂性和一旦事情开始可靠地工作时的快乐。它还显示了 ESP-1 模块用于其原始目的的少数情况之一:作为一种通过完整 WiFi 和 TCP 堆栈添加 WiFi 功能的简单方法，而不会增加主 CPU 的负担。

(谢谢，鲍尔德沃)