# 使用这款 NFC 多功能工具搜寻 NFC 信号

> 原文：<https://hackaday.com/2022/10/17/hunt-down-nfc-signals-with-this-nfc-multi-tool/>

NFC 黑客攻击可能是一项艰巨的任务，需要许多专门的工具、大量的协议和大量不同的设备。[ElectronicCats]做了大量工作，试图通过创建一个开源、硬件认证的 NFC 工具来实现这一研究，该工具名为 [HunterCatNFC](https://github.com/ElectronicCats/HunterCatNFC) ，可以读取和模拟大量的 NFC 设备。

HunterCatNFC 设备是便携式和独立的，带有 LED 指示灯，可以提供各种模式的信息，并反馈正在接收的数据。HunterCatNFC 的核心是一个恩智浦 PN7150 NFC 控制器芯片，用于处理 NFC 通信。主处理控制器是一个微芯片 SAMD21，它也提供 USB 功能，整个设备由 3.7V 150mAh 锂离子电池供电。

HunterCatNFC 有三种主要模式，“仿真”、“读/写”和“对等”。仿真模式允许 HunterCatNFC 模仿无源 NFC 设备的功能，仅在 NFC 读取器发出请求时做出响应。读/写模式允许它模拟 NFC 读取器或写入器，能够与附近的无源 NFC 设备通信。对等模式赋予设备双向通信的能力，例如，在两个 HunterCatNFC 设备之间。

我们在之前已经报道过 [NFC 黑客攻击，包括](https://hackaday.com/2020/08/23/breaking-smartphone-nfc-firmware-the-gory-details/) [Flipper Zero](https://hackaday.com/2021/10/04/whats-on-your-bank-card-hacker-tool-teaches-all-about-nfc-and-rfid/) 。HunterCatNFC 是 NFC 黑客工具库的一个很好的补充，有一些非常好的[文档](https://github.com/ElectronicCats/HunterCatNFC/wiki)可供学习。对于那些不想把自己的电路板送出去印刷和组装的人，[ElectronicCats]有出售的[。](https://electroniccats.com/store/hunter-cat-nfc/)

休息后的视频！

 [https://www.youtube.com/embed/_y17rtbAfdA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_y17rtbAfdA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

