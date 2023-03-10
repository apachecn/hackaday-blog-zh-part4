# 在没有 USB-C 支持的笔记本电脑上伪造 USB-C 支持

> 原文：<https://hackaday.com/2020/03/27/faking-your-way-to-usb-c-support-on-laptops-without-it/>

加密狗问题没完没了吗？我们认为问题出在所有那些非 USB-C 设备上，这些设备希望与只有 USB-C 端口的新 Macbooks 配合良好。但是，那些想要使用传统设备的 USB-C 设备怎么办呢？

现在有些人会说，只要给自己找一根 USB-C 转 USB-A 线就行了。但这违背了 USB-C 的目的，即*一根电缆统治一切*^([1](#footnote_1))。[马塞尔·瓦拉洛]决定让他的 2011 年 Macbook 没有软件狗和适配器电缆，方法是[将 USB-C 端口焊接到主板上的 USB 2.0 接口上](https://www.marcelvarallo.com/adding-usb-c-to-a-late-model-2011-macbook-pro-sorta/)。

这怎么可能呢？诀窍是从 USB-C 转 USB 3 适配器开始。这款老式 Macbook 没有 USB 3，但该协议的规范保持了与 USB 2 的向后兼容性。[Marcel]介绍了将适配器从外壳中取出、切掉非常重要的 C 部分，并找到合适的信号以路由到主板上现有的 USB 端口的过程。

[1]哦，我的天，这是什么说法！正如我们在 Raspberry Pi USB-C 失败事件中看到的那样，[实际上有几种不同类型的 USB-C 电缆](https://hackaday.com/2019/07/16/exploring-the-raspberry-pi-4-usb-c-issue-in-depth/)，除了连接器外壳上模制的神秘图标之外，它们在外表上看起来都非常相似。但从好的方面来看，你可以从任何一个方向插入任何一端，这样它就可以工作了。