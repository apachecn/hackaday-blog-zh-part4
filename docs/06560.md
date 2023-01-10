# 面向传统设备的整洁的 USB-C 转换

> 原文：<https://hackaday.com/2020/05/12/neat-and-tidy-usb-c-conversions-for-legacy-devices/>

USB-C 已经上市好几年了，现在终于开始占据市场了。许多新的笔记本电脑只配备了较新的端口，因此很难使用传统的 USB-A 设备。[Matt]不喜欢摆弄软件狗和集线器，所以着手将一些旧硬件转换成新标准。(视频，嵌在下面。)

[Matt]首先着手黑掉一个罗技无线鼠标加密狗，剥开原来的 USB A 连接器以接触到里面的 PCB。然后获得 USB C 分线板，并将 USB-C 连接器中的相关引脚焊接到原来的 USB-A 连接器焊盘上。不幸的是，分线板被配置为主机设备，不适合外围设备。用 VCONN 和 CC1 引脚上的下拉电阻代替上拉电阻可以纠正这一问题。mod 完成后，鼠标枚举并通过 USB-C 完全运行。然后用一点 Sugru 将所有东西包装整齐。

[Matt]然后通过其他几个类似的 mod 发展到其他硬件，分享关于如何使东西尽可能整洁和有用的有用提示。这是一个整洁的黑客，可以让你的新笔记本电脑的用户体验更少痛苦。USB-C 模块正变得越来越普遍，我们已经看到了很多由于电源传输规范而对烙铁所做的事情。

 [https://www.youtube.com/embed/V-vFtiDYiIw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/V-vFtiDYiIw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

