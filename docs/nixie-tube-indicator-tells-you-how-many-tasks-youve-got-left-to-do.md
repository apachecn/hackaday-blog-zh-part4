# 数码管指示器告诉你还有多少任务要做

> 原文：<https://hackaday.com/2021/11/17/nixie-tube-indicator-tells-you-how-many-tasks-youve-got-left-to-do/>

对于忙碌的人来说，跟踪待办事项清单上的所有任务本身就是一项令人生畏的任务。幸运的是，有软件可以帮助你保持有序，但拥有一个实体物品也总是好的。受到一些漂亮的谢妮时钟设计的启发，[Bertrand Fan]决定[制作一个谢妮指示器](https://bert.org/2021/11/16/iot-nixie-tubes/)，它会告诉他待办事项列表上有多少未完成的项目，随着每个已完成任务的倒计时，给人一种即时的满足感。

这个项目的任务管理部分是一个叫做 Todoist 的在线工具。这个程序附带了一个有用的 Web API，允许你把它连接到你自己的软件项目并交换数据。[Bert]编写了一些代码，从他的待办事项列表中提取未完成任务的数量，并将其发送到驱动数码管的 ESP8266 D1 Mini。考虑到让这样的设备直接连接到互联网的安全隐患，他设置了一台 Mac Mini 作为网关，通过 WiFi 连接到 ESP8266，通过 VPN 连接到 Todoist 服务器。

这个小小的 ESP 电路板位于一个 3D 打印的盒子里，还有谢妮驱动电路和一个用来固定电子管的插座。贴在正面的瓷砖让它看起来更加坚固、奢华，与闪亮的玻璃和金属显示设备相得益彰。数码管的局限性将显示的任务数量限制在 9 个，但我们想象这实际上可能有助于防止[Bert]让自己承担过多的任务。毕竟，如果你在一天结束时不能达到那个令人满意的“零”，那么拥有这个设备又有什么意义呢？

虽然如今谢妮电子管大多与花哨的时钟联系在一起，但我们已经看到它们被用于各种其他用途，例如[跟踪 3D 打印机灯丝](https://hackaday.com/2019/05/09/old-nixie-display-rides-again-as-3d-printer-filament-meter/)，给 20 世纪 40 年代的收音机添加[显示屏](https://hackaday.com/2019/03/17/making-a-1940s-radio-digital-with-nixies/)，或者干脆[根本不显示任何有用的东西](https://hackaday.com/2018/09/29/this-nixie-device-is-useless-but-pretty/)。

 <https://bert.org/assets/posts/nixie/todo.webm?_=1>

[https://bert.org/assets/posts/nixie/todo.webm](https://bert.org/assets/posts/nixie/todo.webm)