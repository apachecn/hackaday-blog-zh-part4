# raspberry Pi Pico“Modchip”解锁 GameCube

> 原文：<https://hackaday.com/2022/07/05/raspberry-pi-pico-modchip-unlocks-the-gamecube/>

就销量而言，GameCube 是任天堂表现最差的家用游戏机之一已经不是什么秘密了。你可能会说，竞争加剧意味着这款古怪的小机器的销量注定达不到该系统传奇的前辈，但这并没有阻止 Wii 在几年后的销量超过它五倍。尽管如此，GameCube 发布了足够多令人难以置信的游戏，该系统仍然享有相当大的粉丝群。

现在，[随着[webhdx]](https://github.com/webhdx/PicoBoot) 发布 PicoBoot，我们怀疑 GameCube 即将获得全新一代的粉丝。这个开源项目只需要一个 Raspberry Pi Pico、一些跳线和一个广泛可用的第三方 SD 卡适配器，就可以绕过控制台的原始 BIOS，因此它可以直接启动到用户选择的任何自制应用程序。由于执行这种修改是如此的便宜和容易，如果它为 GameCube 自制软件开发开启了某种复兴，我们也不会感到惊讶。

[![](img/4e54e2a48f41deff2005162601835752.png)](https://hackaday.com/wp-content/uploads/2022/07/picoboot_detail.jpg)

Installation takes just five wires.

在休息后的视频中，*Macho Nacho Productions*[的【Tito】提供了这个新项目](https://www.youtube.com/watch?v=qwL4ZSa0xMo)的概要，包括一个奇妙的分步安装指南，涵盖了从将跳线焊接到控制台主板到在 Pico 上安装固件的所有内容。然后，他演示了如何将控制台引导到各种社区开发的前端和工具中，展示了这种修改是多么的通用。虽然有些人会认为这只不过是运行盗版游戏的一种更简单的方式，但我们不禁对未来的发展感到兴奋，因为让自己的代码在系统上运行是如此容易。

好吧，也许这不是*那么*容易。为了焊接最终蜿蜒到 Pi Pico 的 GPIO 引脚的五根导线，您需要将控制台一直拆到主板。这本身还不算太糟糕，但不幸的是，要接触到其中的两个连接，你需要移除系统的巨大散热器——这意味着如果你不想让你的 GameCube 变成 GameCrisp，你需要清理旧的粘性散热垫并应用新的散热垫。这不会吓跑普通的黑客读者，但可能会让那些不太会用熨斗的人暂停一下。

PicoBoot 的发布紧随 Raspberry Pi Pico 不仅可以用作 N64 闪存车还可以用作[增压 PlayStation 存储卡](https://hackaday.com/2022/06/13/raspberry-pi-pico-replaces-playstation-memory-card/)的披露之后。使用定制的 RP2040 板，这些项目都将得到显著改善，毫无疑问，这是它们最终的发展方向，但低成本微控制器开发板在其原始形式下的能力令人印象深刻。尤其是现在[有了 WiFi 版](https://hackaday.com/2022/06/30/raspberry-pi-pico-w-adds-wireless/)。

 [https://www.youtube.com/embed/qwL4ZSa0xMo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qwL4ZSa0xMo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

