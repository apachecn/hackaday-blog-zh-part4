# 每天早上都有一份新的 E-Ink 报纸送来

> 原文：<https://hackaday.com/2021/04/11/a-fresh-e-ink-newspaper-delivered-every-morning/>

[Greg Raiz]最近开始让早上边吃早餐边看多份报纸变得容易起来。受一个类似项目的启发，他制作了一份挂在墙上的电子墨水报纸，每十分钟发布一次最新消息。

该项目从配置为瘦客户端的 32 英寸 Visionect 电子墨水显示器开始。由于低功耗电子设备，电池寿命可以在几个月内测量，这里的大部分工作都集中在后端。运行在本地 NAS 服务器上的 docker 容器通过 freedomforum.org 收集报纸，将它们格式化以适合显示器的纵横比，然后提供给用户。[Greg]真的试图保留这些出版物头版的设计和思想，因为传统的报纸版面通常是手工设计的。

我们喜欢这个项目的简单性和“它只是工作”的感觉，因为没有按钮，电线或任何你需要摆弄的东西。[Greg]指出，它也可以用于其他目的，我们很想看到一个大型日历[，比如这个电子墨水日历](https://hackaday.com/2020/11/19/e-ink-calendar-paves-a-path-for-all/)，或者甚至是[这个电子墨水笔记本电脑](https://hackaday.com/2021/03/12/e-ink-laptop-first-steps/)的 32 英寸版本。休息之后，代码在[的 GitHub](https://github.com/graiz/newsprint) 上，还有一段视频。

 [https://www.youtube.com/embed/gECj1AE9D2c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gECj1AE9D2c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

