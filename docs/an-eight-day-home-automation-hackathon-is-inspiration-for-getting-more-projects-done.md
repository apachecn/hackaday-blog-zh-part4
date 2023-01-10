# 为期八天的家庭自动化黑客马拉松是完成更多项目的灵感

> 原文：<https://hackaday.com/2020/01/24/an-eight-day-home-automation-hackathon-is-inspiration-for-getting-more-projects-done/>

没有什么比截止日期更能去除多余的东西，抓住问题的核心了。也许我们都应该以 Interpreet 为榜样，停止考虑让我们的家实现自动化，只需要在为期八天的黑客马拉松中实现它。他在 2019 年 Hackaday 超级大会上的讲话涵盖了他在八天内完成的[零部署家庭自动化构建](https://www.youtube.com/watch?v=R_PMF2TbCLo)，这是他从一个大陆搬到另一个大陆的前奏。

Hackaday 自己的 Inderpreet Singh 发现自己连根拔起，从印度的家搬到加拿大多伦多的 Centennial College 教书。他需要一种方法从远处监视他的家，这个游戏的名字叫 IoT。当唯一的选择是“现在有效的方法”时，你可以学到很多简单的解决方法。

他选择了熟悉的硬件来工作，ESP8266 构成了大部分节点，Raspberry Pi 作为设置的中心枢纽。他选择使用 WiFi 在他的系统上的所有节点之间进行通信，因为硬件是健壮且可用的。考虑到安全性，他通过获取额外的接入点作为自动化网络，将自动化系统与日常使用的 WiFi 系统分开。Raspberry Pi 充当了某种路由器；它的以太网端口连接到物联网设备的 AP，而板载 WiFi 用于连接到家中的主 AP，以连接到更广泛的互联网。

该系统的软件建立在由 Python Flask 应用程序提供服务的 REST API 之上。许多人主张使用 MQTT，但是 Inderpreet 对该协议的测试并不成功，因为他打算使用的代理不再可用。他的系统设计的一个有趣的部分是，所有节点将定期检查；这允许他们询问他们需要采取的行动，但也允许系统立即检测出故障节点。我见过埃利奥特·威廉姆斯使用类似的技巧，他给所有 MQTT 设备分配一个“ping”主题，让它们报告自己的 IP 地址。拥有一个系统来查询和确保每个节点的健康是从这个演讲中得到的一个大提示。

 [https://www.youtube.com/embed/R_PMF2TbCLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/R_PMF2TbCLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



安装系统是我们很多人都会遇到的问题。Inderpreet 没有时间让系统隐形。他的母亲不喜欢他在墙上打洞，把零件粘在门上，但是最后期限到了，系统开始运行了。美学可以随着时间的推移而改进，最好留到概念验证之后。

任何项目都很容易陷入规划阶段。这一冒险展示了潜水的力量，并用最少的可行产品建立你的立足点。试一试，你会发现从长远来看，你会完成更多的项目。