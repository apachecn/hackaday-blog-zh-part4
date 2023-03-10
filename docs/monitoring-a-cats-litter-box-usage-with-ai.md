# 用人工智能监控猫砂盒的使用

> 原文：<https://hackaday.com/2022/08/30/monitoring-a-cats-litter-box-usage-with-ai/>

【Estefannie】是一个骄傲的猫主人，但是她的一只猫有吃塑料的坏习惯。这意味着她需要留意那只猫的大便，但家里有两只猫，很难知道谁做了什么。因此，她发明了一个人工智能系统[来记录她的猫上厕所的次数，让她安心。](https://www.estefannie.com/blog/f63kkhwgq56u76hjsysy1moy5ttuuf)

这并不是最迷人的项目——[Estefannie]指出，她用垃圾箱拍摄了超过 5 万张她的猫的照片，以训练微软 Azure 的定制视觉模型。但经过一些工作后，当从一台黑色相机中获得图像时，它可以很容易地识别出哪只猫正在使用猫砂盒。然后，该系统通过猫在猫砂箱中度过的时间来区分 1 号和 2 号。它并不完美，但很有效。

树莓 Pi 运行一个节点。JS 服务器整理结果，搭配网站前端，方便数据展示。这样，任何在(Estefannie 的)WiFi 网络上的人都可以通过浏览器看到谁做了什么。我们之前已经看到过[猫砂箱被放到物联网](https://hackaday.com/2019/08/28/cat-litter-tray-joins-the-internet-of-things/)上，我们甚至还看到有人黑掉了[猫砂箱的 DRM](https://hackaday.com/2018/09/04/doing-logic-analysis-to-get-around-the-catgenies-drm/) 。

 [https://www.youtube.com/embed/6jDDZjSyXpc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6jDDZjSyXpc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

