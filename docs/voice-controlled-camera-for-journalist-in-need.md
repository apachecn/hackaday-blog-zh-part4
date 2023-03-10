# 为有需要的记者准备的声控摄像机

> 原文：<https://hackaday.com/2018/12/29/voice-controlled-camera-for-journalist-in-need/>

在进入多伦多百年学院的新闻项目之前，[卡罗琳·皮奥罗]是一名空中飞人表演者。不幸的是，2005 年的一次事故结束了她作为空中专家的职业生涯，当时她切断了脊髓，导致她肩部以下瘫痪。在语音转文本技术领域有很多选择可以让她在电脑上写作，但当她试图找到一个可以让她用声音指向并拍摄 DSLR 相机的商业产品时，她一无所获。

[![](img/c643dee698a9b7787c2d4ff98bf8f1ab.png)](https://hackaday.com/wp-content/uploads/2018/12/voicecam_detail.jpg)【Taras Slawnych】听说【Carolyn】需要特殊的摄影器材，觉得他有经验可以做点什么。有了一个 Arduino 和几个伺服系统来驱动云台机构，他想出了[一个小装置，Carolyn 现在可以用它来控制安装在她轮椅](https://www.thestar.com/news/gta/2018/12/23/this-journalist-needed-a-voice-operated-camera-but-there-was-nothing-on-the-market-so-he-made-her-one.html)的一个手臂上的佳能相机。仍有一些改进的空间(值得注意的是，目前焦点不能通过语音控制)，但即使在这种早期形式下，这个小工具也引起了佳能加拿大分部的注意。

操作员衬衫上带有领夹式麦克风，设备 3D 打印外壳内的 Arduino 可接收和解释简单的语音命令，如“右”和“左”。Arduino 然后将相应的伺服电机移动设定的度数。这不允许特别精细的定位，但是当结合轮椅本身的运动时，给用户一个可接受的控制水平。[Taras]表示，整个设置由电动轮椅的 24 VDC 电池供电，通过降压转换器将它转换为 Arduino 和伺服系统的安全电压。

[正如我们多年来所看到的](https://hackaday.com/2017/09/11/these-twenty-assistive-technologies-projects-won-1000-in-the-hackaday-prize/)，辅助技术是[黑客似乎有本事为他人的生活做出重大贡献的领域之一](https://hackaday.com/2018/02/07/steam-fabrikarium-mumbai/)(有时甚至是他们自己)。许多身体残疾的高度个性化性质，以及个人特有的具体问题和需求，可能[使开发这种商业设备](https://hackaday.com/2018/07/05/shooting-for-the-first-time-with-help-from-a-raspberry-pi/)变得困难。但是，只要黑客愿意贡献他们的时间和知识来创造定制的辅助硬件，就还有希望。

 [https://www.youtube.com/embed/HtOj2uKgcU0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HtOj2uKgcU0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/3N3c1zXT_os?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3N3c1zXT_os?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢菲利普的提示。]