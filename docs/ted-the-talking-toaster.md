# 会说话的烤面包机泰德

> 原文：<https://hackaday.com/2019/12/23/ted-the-talking-toaster/>

[8 比特和一个字节]背后的团队已经建造了一个会说话的烤面包机。更准确地说，他们用一些硬件组件改造了现有的烤面包机，使它看起来会说话，并对用户发火。虽然实际的烤面包机功能对于构建来说不是必需的，但它确实允许项目有一个更异想天开的氛围。

该项目使用一个树莓 Pi 3 和一个谷歌 AIY 套件，包括一顶帽子，麦克风和扬声器。伺服系统在帽子的帮助下控制烤面包机眉毛的运动。一些装饰材料，如眼睛和管道清洁器，有助于将会说话的烤面包机的其他功能带入生活。

聊天机器人的控制流利用 Google 的语音到文本从音频输入中提取文本，利用 [Dialogflow API](https://cloud.google.com/dialogflow/docs/quick/api) 匹配意图，利用文本到语音将可能的答案传送回 Raspberry Pi 以通过扬声器播放。他们还使用 [Remo.tv](https://remo.tv/join/qcqrl9u) 向任何人在线直播烤面包机的更新，允许聊天室的用户直接与 Ted 对话。

虽然 Ted 的交流可能非常有限，但他现在在线互动的次数肯定是无限的！

 [https://www.youtube.com/embed/XEd3NvMYt48?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XEd3NvMYt48?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

