# TI EZ430-Chronos 转变为可穿戴医疗警报

> 原文：<https://hackaday.com/2020/12/22/ti-ez430-chronos-turned-medical-alert-wearable/>

早在当前智能手表热潮之前，德州仪器就发布了 eZ430-Chronos。即使按照 2010 年的标准，它也相当笨重。它简单的液晶显示屏和少量的按钮也限制了它可以实际执行的“智能”任务。但它确实有一个优点:它的 SDK 允许用户创建一个定制的固件来满足他们的具体要求。

近十年来，我们没有看到任何人重新使用 eZ430-Chronos，但这并没有阻止[ogdento]将它变成一个为生病的家人定制的提醒设备。手表上一个简单的两键程序将向预先定义的联系人列表发送电子邮件和短信，所有这些都不涉及第三方，也不必为服务合同付费。也许最重要的是，相对节能的 eZ430 不需要像现代智能手表那样每周甚至每天充电。

为了使设备尽可能简单，[ogdento]检查了股票固件的源代码，并注释掉了除显示时间之外的所有功能。手表的菜单被精简到最少，引入了一个新的提醒功能，可以使用设备的 915 MHz CC1101 无线电发送信息。

[![](img/0133da32692fcfeab0fedcae859f97f6.png)](https://hackaday.com/wp-content/uploads/2020/12/ez430alert_detail.png)

Messages and recipients can easily be modified.

显示屏甚至会在相应的按钮旁边显示“帮助”,这样就不会混淆了。发送警报需要第二次按键，甚至还有一个条款规定，如果按钮被意外按下，就可以取消警报。

在接收端，[ogdento]正在使用一个 Raspberry Pi，它自己的 CC1101 无线电插入 USB 端口。当运行在 Pi 上的 Python 脚本接收到来自 eZ430 的传输时，它开始处理要向其发送消息的接收者列表。快速浏览一下源代码就可以看出，如果你想组装自己版本的系统，提供自己的联系人列表是很容易的。

[在](https://hackaday.com/2017/09/04/hackaday-prize-entry-elderly-autonomous-fall-detection/)之前，我们已经见过定制警报硬件，但正如[ogdento]所指出的，使用 eZ430-Chronos 提供了一个相当大的优势，因为它是一个交钥匙平台。它穿着舒适，可靠，而且相当坚固。虽然有些人会反对[信任独立开发的代码来完成如此重要的任务](https://hackaday.com/2020/04/09/what-does-a-dependable-open-source-ventilator-look-like/)，但至少硬件是一个已经解决的问题。