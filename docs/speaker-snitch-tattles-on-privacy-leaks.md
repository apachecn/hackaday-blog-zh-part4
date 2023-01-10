# 议长告密泄露隐私

> 原文：<https://hackaday.com/2020/12/09/speaker-snitch-tattles-on-privacy-leaks/>

一位明智的参议员曾经指出，民主在雷鸣般的掌声中消亡。同样，这也是隐私死亡的方式，因为我们心甘情愿地邀请越来越多的智能设备进入我们的家，这些设备是由那些往往不考虑我们最佳利益的公司建造的。如果你不愿意把所有这些公认有用的设备扔出家门，但仍然想关注它们在做什么，那么，[Nick Bild] [有一个方便的项目，让你在它们试图访问网络](https://github.com/nickbild/speaker_snitch)时关注它们。

该设备是建立在一个树莓 Pi 上的，它在家庭网络中充当这些设备的中间人。他们试图发送的任何流量都通过 Pi 发送，Pi 通过 Python 脚本嗅探流量，并能够检测他们何时访问他们的云服务。从那里，Pi 向连接到 LED 的物联网 Arduino 发送警报，LED 在智能设备活动期间点亮。

这是一个有趣的构建，因为众所周知，许多智能设备甚至不用说出暗语(如“嘿，谷歌”等)就能监听日常对话。)这是让设备在任何特定时刻都处于非活动状态的一种很好的方式。然而，这并不是一种保证隐私的万无一失的方法，因为许多设备可能正在访问其他服务，而且还有其他设备[甚至已知带有隐藏硬件](https://hackaday.com/2019/03/11/what-hardware-lies-beneath-companies-swear-they-never-meant-to-violate-your-privacy/)。

 [https://www.youtube.com/embed/8SCS7iIHqxg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8SCS7iIHqxg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

