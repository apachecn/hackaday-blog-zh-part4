# 解开 SEGGER J-Link V9 调试探针

> 原文：<https://hackaday.com/2020/12/30/unbricking-a-segger-j-link-v9-debug-probe/>

去年[Emil]发现他们的一个 SEGGER J-link 调试探针突然停止工作。这很尴尬，不仅因为在线调试器是嵌入式固件开发中至关重要的设备，还因为它们并不便宜。这导致[Emil]将设备拆开[以找出问题所在](https://uglyduck.vajn.icu/ep/archive/2019/05/Unbricking_a_SEGGER_J_Link_v9_debug_probe.html)。

检查 PCB 上的电压后，似乎没有明显的问题。PCB 上的标签连接式 JTAG 接头似乎是一个很好的第二站，只需要一点点工作来逆向设计精确的引脚排列，并连接一个 ST-Link V2 在线调试器，以便与 PCB 上的 STM32F205RC MCU 进行通信。这导致了有趣的发现，显然 MCU 的闪存 ROM 似乎丢失了固件数据。

幸运的是[Emil]能够闪回互联网上的固件版本，让 J-Link 设备再次工作。然而，这并不是故事的结尾，因为在这之后，由于缺少不属于固件映像的引导加载程序，SEGGER 软件无法更新设备上的固件。

进一步挖掘，Emil 发现了一大堆有趣的细节，不仅是这些 SEGGER J-Link 设备，还有许多克隆设备，以及 SEGGER 让人们购买新版本调试探针的有趣方式。

(感谢 Zelea 的提示)