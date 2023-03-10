# Tweetbot 表达推特情绪

> 原文：<https://hackaday.com/2019/03/16/tweetbot-expresses-twitter-emotions/>

当阅读文本交流时，很难准确地理解某种情感意图。个人在这方面可能更好或更差，有时出错时会有令人捧腹的结果。不管怎样，人类能做的任何事情，机器最终都会做得更好。出于这个目的，Tweetbot 在这里对 Twitter 做出情绪反应，所以你不必这样做。

该机器人通过蓝牙链接接收推文，由 PIC32 处理，并在一个小 TFT 屏幕上显示。PIC 然后分析推文的情感内容，然后将结果发送到第二个 PIC32，第二个 PIC 32 在第二个 TFT 屏幕上显示表情，创建机器人的脸。根据检测到的情绪，不同的 led 也会闪烁——绿色表示积极的情绪，黄色表示悲伤，红色表示愤怒。

最终的机器人能够展示 8 种独特的情绪状态，远远超过典型的脸书评论者只能表达肆无忌惮的愤怒。随着机器人包装显示器，多个微控制器，甚至电机驱动，我们想象团队在项目的开发中学到了很多。

该项目是[Bruce Land]的 ECE 4760 课程的产物，该课程在过去向我们展示了许多伟大的黑客技术—[自行车声纳是我们最喜欢的技术之一](https://hackaday.com/2017/01/11/this-bike-sonar-is-off-the-chain/)。休息后的视频。

 [https://www.youtube.com/embed/OoaDNdVuM5I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OoaDNdVuM5I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

