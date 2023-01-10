# 专为帮助您在家工作而设计的压力监视器

> 原文：<https://hackaday.com/2021/08/11/a-stress-monitor-designed-specifically-to-help-you-work-from-home/>

关于在家工作，人们的情绪很复杂。一些人喜欢它，并像以前一样蓬勃发展，但另一些人则有点难以适应。[Brandon]在过去的 12 年里一直在家工作，但即使在管理这种类型的工作文化这么多年后，他承认这仍然有点压力。他说，他没有足够的时间在任务之间简单地放松和喘口气，如果他不花一些时间让自己平静下来，他每天工作中的琐事会让他的压力水平上升。他认为他可以做点什么来监控自己的压力水平，提醒自己休息一下，结果令人印象深刻。

他开发了一个系统来监控他的心率和他房间的环境噪音水平，并使用这些指标来衡量压力。如果他的心率或环境噪音水平超过某个阈值，那么他会给自己发送一条短信，提醒自己放松并休息一下。你可能已经见过[人们用心率来衡量压力](https://hackaday.com/2013/03/20/measuring-meditation-with-a-heart-rate/)，但是你可能不太熟悉用声音。[Brandon]基本上认为声音传感器会检测他是否开始长时间[咆哮，或者他是否正在参加一个变得太热的缩放会议](https://hackaday.com/2020/07/15/quickly-mute-and-unmute-yourself-using-the-physical-mute-button/)。我们认为这很棒。

[布兰登]使用现成的胸带心率监测器来节省自己的时间，试图[建立自己的](https://hackaday.com/2014/02/13/arduino-powered-ecg-informs-users-of-their-death/)。该设备通过蓝牙将心率数据发送到 nRF52840，然后使用 Blues 无线 Notecard 将数据推送到云端。Notecard 还提供数据加密，这让[Brandon]更加放心，因为他知道他的生物数据不会在没有任何保护的情况下在云中流动。这当然不是医疗级别的加密，但它给了他一点安慰。所有这些数据都在他定制设计的网络应用程序中进行处理，当达到适当的阈值时，他会使用 Twilio 向自己发送一条短信，提醒他放松一下。

在他的下一次迭代中，[布兰登]可能会尝试制作自己的心率监测器。但在那之前，大家注意安全，记得需要的时候休息一下。

 [https://www.youtube.com/embed/Ec8bH7NI9T8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ec8bH7NI9T8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

