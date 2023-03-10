# 野外 DIY 自主割草机

> 原文：<https://hackaday.com/2020/01/10/diy-autonomous-mower-in-the-wild/>

修剪草坪是我们大多数人都希望有一个机器人来做的重复性工作之一。[肯尼·特鲁塞尔]割草比大多数后院都要费力，所以他[改装了一台乘驾式割草机](https://www.youtube.com/watch?list=PLIsYv3gzZOt9N9yZmpI_WYiMaBQ6HazOG&v=jKDqPt3H2bQ&feature=emb_title)来独自处理多英亩的田地。

割草机开始时是标准的零转弯割草机。它的大脑由运行 Ardurover 的 PixHawk 板组成，Ardurover 是地面车辆的 Ardupilot 衍生产品。导航由 RTK GPS 模块提供，该模块通过 Adafruit LoRa 羽毛板从固定基站获得误差校正，以达到厘米级的精度。为了控制割草机，[Kenny]用线性致动器取代了控制杆中心的气动冲击。

到目前为止，[肯尼]一直在使用割草机割草，面积达 5-18 英亩，对于人工操作者来说，这是一项非常耗时的工作。现有的安全电路中增加了一个继电器，只允许割草机在座位上有重量时工作。该继电器直接连接到 RC 接收器，并由手持式 RC 发射器控制。如果发射器失去信号，它也会停止割草机。为了设置割草任务，[Kenny]使用 Ardupilot 任务规划器，他为此编写了一个自定义命令行实用程序，为割草机创建一条同心路线，以完全覆盖一个定义的区域。他制作了一系列关于这个过程的视频，这对任何想做同样事情的人来说都非常方便。我们期待一个包含所有最新更新的新视频。

这台割草机已经强劲运行了两年，但就记录的小时数而言，它比这台已经使用了 20 多年并且仍然依靠英特尔 386 处理器运行的老牌机器人割草机强不了多少。

 [https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLIsYv3gzZOt9N9yZmpI_WYiMaBQ6HazOG](https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLIsYv3gzZOt9N9yZmpI_WYiMaBQ6HazOG)

