# 宜家搁板成为儿童友好型 MP3 播放器

> 原文：<https://hackaday.com/2021/02/12/ikea-shelf-becomes-kid-friendly-mp3-player/>

宜家的平板包装家具因其模块化和低成本而长期受到制造商的欢迎，使其成为古怪实验和定制的理想选择。[克劳斯]就是这样一个人，他用一个基本的书架为他的孩子制作了一个有趣的 MP3 播放器。

音乐由 NodeMCU ESP8266 处理，与 VS1053 音频板协同工作。VS1053 是一款高性能芯片，能够解码各种原始和压缩音频格式以及 MIDI，但在这里它用于读取 SD 卡和播放 MP3。RC522 用于读取 RFID 卡来触发各种曲目，允许孩子们通过简单地在书架上放置标签来选择歌曲。使用廉价的 PAM8302 放大器和扬声器来输出音乐。所有硬件都整齐地安装在 LACK 拉克搁板内，由于主要采用纸板结构，这项工作非常简单。

RFID 卡比我们通常认为的更有趣，我们已经看到一些类似的产品。休息过后,【克劳斯的】孩子尽情摇摆的视频。

 [https://www.youtube.com/embed/FcALmyrhR3w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FcALmyrhR3w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

