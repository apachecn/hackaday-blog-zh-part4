# Windows 实用工具帮助识别串行端口

> 原文：<https://hackaday.com/2019/05/22/windows-utility-helps-id-serial-ports/>

不起眼的串行接口已经存在了很长时间，并且在可预见的将来还会以这样或那样的形式存在。在计算机只有一个或两个 COM 端口的时代，很容易跟踪。然而，在这个 USB 可编程微控制器的时代，很可能你已经得到了来自 wazoo 的 COMs。谢天谢地， [[Amr Bekhit]开发了一个实用程序来帮助解决这个问题。](https://helmpcb.com/software/serial-port-monitor)

[Amr 的]实用程序被称为串行端口监视器，它做它在 tin 上所说的事情。当在设备管理器中枚举新的串行端口时，会弹出一个系统托盘通知，指出新连接的 COM 端口的编号。此外，它还维护了一个按最新端口排序的端口列表，并提供了一个右键菜单，允许启动各种终端程序。

这是一个放在口袋里的有用工具，尤其是在同时对多个 devboards 进行编程时，或者当您发现自己在处理一堆串行设备时。

顺便说一句，如果你发现自己一直对 Windows 上的 USB 转串行适配器感到头疼，[这可能就是你的问题](https://hackaday.com/2016/02/01/ftdi-drivers-break-fake-chips-again/)。黑客快乐。

脚注:鉴于这篇文章，作者想正式向[Cosmos2000]道歉，因为他在主编程平台上永久禁用了 COM1。抱歉，朋友。