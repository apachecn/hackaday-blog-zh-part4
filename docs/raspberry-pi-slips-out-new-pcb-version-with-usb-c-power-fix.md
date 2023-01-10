# Raspberry Pi 推出带 USB C 电源修复的新 PCB 版本

> 原文：<https://hackaday.com/2020/02/23/raspberry-pi-slips-out-new-pcb-version-with-usb-c-power-fix/>

当 Raspberry Pi 的人在他们的水果味单板电脑系列中发布一款新机型时，这总是一件令人非常感兴趣的事情。树莓 Pi 4 给配方带来了一些重大变化:例如，他们转向了 ~~mini~~ micro HDMI 和 USB-C 电源插座。虽然早期采用者获得了 Pi 4s 中的一个，但他们感到震惊，如果他们除了最基本的 USB C 电源线之外，其他都没有，设备就不会通电。现在*注册*有消息说，他们已经悄悄推出[一个更新版本的板，包含这个问题的修复](https://www.theregister.co.uk/2020/02/21/pi_4_fixed/)。

我们的同事 Maya Posch 深入研究了 USB C 规范，[在当时](https://hackaday.com/2019/07/16/exploring-the-raspberry-pi-4-usb-c-issue-in-depth/)发表了精辟的分析，证明故障在于智能 USB C 电源用来确定供电的检测电阻的配置。因为增加了一个表面贴装电阻，这个问题根本不存在，我们猜测他们就是这样解决的。

不过，如果你有一块较旧的主板，也没必要绝望。它们仍然会像往常一样使用所谓的“哑”电源和电缆工作，同时我们确信未来的 Pi 板将会非常关注它们的 USB 电源电路。