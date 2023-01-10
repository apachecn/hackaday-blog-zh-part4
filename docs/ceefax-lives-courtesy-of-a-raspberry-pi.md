# 西法克斯活着！(由树莓派提供)

> 原文：<https://hackaday.com/2022/01/07/ceefax-lives-courtesy-of-a-raspberry-pi/>

随着模拟电视从记忆中滑落，它的一个方面被一群爱好者深情地记住了。图文电视是一种在帧消隐期间以数字方式编码的电子视频数据信息服务，带有解码器芯片的电视机可以提供多页新闻和其他服务，所有这些都以色彩鲜明的块图形显示。随着模拟电视的消亡，它走上了恐龙的道路，但对于[内森·戴恩]来说，他自己的私人版本 BBC 的 CEEFAX 服务使火焰保持不灭。

他对模拟电视有着特殊的热情，因此他有自己的内部频道，由超高频调制器提供服务。他与我们分享了他如何在编写代码抓取 BBC 新闻和天气网站并填充他的现代 CEEFAX 之前实现图文电视服务的故事。在这一切的背后是一个 Raspberry Pi，[一个 vbit-pi 板](https://github.com/peterkvt80/vbit-pi)将图文电视信号注入视频， [raspi-teletext](https://github.com/ali1234/raspi-teletext) 从一组定制的 scraper 脚本派生的源材料创建页面。

我们非常喜欢这个项目，因为虽然[它不是我们遇到的第一个 Pi 图文电视系统](https://hackaday.com/2015/02/13/teletext-on-a-raspi-with-zero-additional-parts/),但使用一个抓取的直播馈送使它成为最有创意的系统之一。

感谢[kwikius]的提示！