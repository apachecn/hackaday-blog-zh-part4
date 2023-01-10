# 如何运行第一代手机网络

> 原文：<https://hackaday.com/2021/06/02/how-to-run-a-first-generation-cell-phone-network/>

复古技术很酷。起作用的复古技术甚至更酷。当我们看到技术在工作时，就把它握在手中，使用它，就好像我们已经回到了过去；那是我们真正感受到历史的时候。为了帮助其他人创建他们自己的小时间异常，[Dmitrii Eliuseev]整理了一个快速的方法来创建自己的高级移动电话系统(AMPS)网络，它可以让一些昨天的经典蜂窝英雄复活。

很少有读者会对这个项目建立在软件定义无线电(SDR)和 [Osmocom-Analog](https://hackaday.com/2018/11/03/revive-that-old-analog-cell-phone-with-sdr/) 项目上感到惊讶，我们之前已经看到过[在 EMF Camp](https://hackaday.com/2018/08/30/gsm-phone-network-at-emf-camp-built-on-raspberry-pi-and-limesdr/) 使用这个项目创建一个更现代的 GSM 网络。过去的项目是基于 LimeSDR 的，但在这里我们看到 USRP 也同样容易得到支持。[Dmitrii]还提供了 AMPS 的简史，包括它一直持续到 2007 年的一些原因！该系统的特点是覆盖范围非常大，而发射塔相对较少，并且音频质量惊人地好。他还讨论了它的缺点，主要是任何拥有扫描仪和正确技术的人都可以调谐到模拟音频并偷听对话。我们必须承认，仅凭这一点，就足以让该体系退休。

这篇文章确实提到，运营自己的手机网络可能存在法律问题，所以一定要查看当地的法规。他还指出，AMPS 足够强大，可以用假负载而不是天线在短距离内工作，这可能有助于避免监管问题。也就是说，SDR 为黑客利用旧的无线协议做什么打开了许多可能性。你甚至可以回到寻呼机为王的时代。或者，如果有线更适合你，我们可以随时推荐[成为你自己的拨号网络服务提供商](https://hackaday.com/2020/05/30/build-your-own-dial-up-isp-now-with-modem-pool/)。