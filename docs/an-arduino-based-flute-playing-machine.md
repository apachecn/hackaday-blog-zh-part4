# 基于 Arduino 的长笛演奏机

> 原文：<https://hackaday.com/2020/01/11/an-arduino-based-flute-playing-machine/>

能够从笛子上转录音乐是一回事，能够让笛子演奏预先写好的音乐是另一回事。后者是[Abhilash Patel]决定在[长笛演奏机](https://www.instructables.com/id/Arduino-Based-Flute-Player-Machine/)中追求的，这是一个基于 Arduino 的项目，使用气流机制和 PVC 管来控制临时长笛产生的音符。它目前能够演奏 17 个音符，从 e 的最低频率开始，刚过两个八度。

为了播放歌曲，音调必须直接编码并上传到 Arduino，用随机音符发生器创作，或者从麦克风检测。虽然机器可以使用真正的长笛，但[Patel]使用的是 PVC 长笛，是用一些长笛演奏知识制作的。

共振频率是基于有效长度，孔的大小和管道直径，所以很难正确调整自制长笛。然而，将长度计算为 *c/2f* ，其中 *c* 是声速(~345 米/秒)，而 *f* 是音符的频率，可以帮助识别孔的位置。[Patel]切割 PVC 管并封闭一端，钻一个 1.5 倍管径的吹孔。吹完笛子后，管子的末端被填满，直到频率与期望的音符完全匹配。

这个洞的覆盖物使用连接到一根连接到伺服系统的电缆上的管道的切屑。电机被隔离在一个盒子里，以保持电线畅通，并且所有区域都能够由 5 V 供电。至于软件，代码主要用于控制风扇何时吹风以及哪些孔被盖住以产生音符。

请听下面视频中来自*泰坦尼克号*的长笛演奏《我心永恒》。现在下一步可能就是让长笛演奏机自动演奏乐谱——想象一下可能性吧！

 [https://www.youtube.com/embed/J8-qwAzsvn4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/J8-qwAzsvn4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

