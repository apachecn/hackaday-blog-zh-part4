# 自动化让你可以不去管你的植物

> 原文：<https://hackaday.com/2021/11/05/automation-allows-you-to-leaf-your-plants-alone/>

盆栽植物面临的最大威胁来自其主人的健忘，但[马赛丽·卡拉诺维奇]创造了一个自动化系统，可以让他的植物不会太渴。在过去的一年里,[马赛丽]一直在记录一个监测和浇灌植物的优雅系统，这个系统现在已经发展成为一个全自动的解决方案。

如果你还没有看过这个项目的早期阶段 [和阶段](https://www.youtube.com/watch?v=RPgxssBxUtw)，它们绝对值得一看。简而言之,[马赛丽]开发了一种浇水系统，该系统使用 I ² C 与土壤湿度、温度和光线传感器进行通信，并控制螺线管，从而根据需要给单个植物浇水。ESP32 充当桥梁，允许通过 HTTP 接口读取传感器和分配水。

在这最后一部分，[马赛丽]将他的供水系统集成到一个家庭自动化系统中。他使用 MySQL 数据库来存储传感器数据和浇水活动的日志，使用 n8n 来自动测量和浇水。如果有些事情不太对劲，系统甚至会给他发一份电报通知，告诉他有些事情不对劲。

如果你认为自动化可能是拯救你的植物免于缓慢死亡的最佳方式，[马赛丽]已经在 GitHub 上分享了他的优秀作品。即使你没有园艺技能，这仍然是如何从头开发家庭自动化解决方案的一个很好的例子。如果你对电视比对园艺更感兴趣，看看马赛丽的 T2 用网络界面代替遥控器的方法！

 [https://www.youtube.com/embed/jLdTUMHOhRE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jLdTUMHOhRE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

