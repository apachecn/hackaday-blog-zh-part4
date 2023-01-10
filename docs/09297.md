# 机器人台球杆可以是你的朋友，也可以是你的敌人

> 原文：<https://hackaday.com/2021/02/24/robotic-pool-cue-can-be-your-friend-or-your-foe/>

[Stuff Here]的谢恩(Shane)一直在寻求用技术取代身体技能，他已经瞄准了八球台球游戏。利用计算机视觉和机电一体化的结合，他创造了一个机器人台球系统，可以通过互联网进行物理台球游戏，或者击败人类玩家。休息后看视频。

做一个好的撞球需要三个独立的步骤。首先，你需要确定最佳击球，然后计算出如何准确地击球以达到预期的效果，最后准确地执行击球。[Shane]的目标是自动化所有这些步骤。对于物理部分，他建造了一个带有机器人尖端的台球杆，只需要用户放置在大约正确的位置，而安装在 Stewart 平台上的气动活塞完成其余工作。一个 [Stewart 平台](https://hackaday.com/2018/10/04/homebrew-linear-actuators-put-the-moves-on-this-motion-simulator/)是一个安装有六个往复杆的三角形板，这给了它所需的运动自由度。杆的基部连接到一组曲柄上，曲柄由安装在球杆后端的伺服机构拉动的张力索驱动。一个可调节的空气系统可以根据需要调节发射功率。

安装在桌子上方的摄像机连接到计算机视觉软件，以收集所需的位置信息。桌角和球杆头上的基准点可以精确确定球袋、球和球杆的位置，理论上可以让机器人打出完美的击球。让这在现实中工作很快变成了一个非常令人沮丧的经历。经过几个小时的调试后，[Shane]跟踪错误到一个微小的被遗忘的测试函数，该函数引入了 5-10 毫米的位置误差，以及球杆中六个伺服系统中的两个没有达到规格。为了确定球杆的垂直位置，增加了 IMU 和固定高度的脚。[Shane]还增加了一个投影仪，将所有需要的信息直接覆盖在桌面上。

在这一点上[Shane]意识到他有所有的部件允许某人通过互联网与他玩台球游戏。他创建了一个简单的网络应用程序，向远程玩家发送视频，然后玩家可以选择[谢恩]应该将球杆放在哪里，然后远程击球。虽然他对这种模式不抱很高的期望，但事实证明这是一种有趣和迷人的体验。

最后一步是让电脑选择镜头。首先，它做了一点伪光线跟踪来编译一个列表，列出所有可能的镜头及其在表格中的效果。然后，它根据距离、精度和球速的组合选择最佳击球。

这可能是[Shane]迄今为止最复杂的一个项目，但只差一点点。事实上，他能够以足够快的速度完成像[数控理发师](https://hackaday.com/2020/07/14/a-robotic-stylist-for-your-lockdown-lengthened-locks/)、[机器人篮球框](https://hackaday.com/2020/09/09/third-times-a-charm-for-this-basketball-catching-robot/)和[爆炸棒球棒](https://hackaday.com/2020/10/27/going-for-the-home-run-record-with-explosive-help/)这样的项目，足以满足每月的上传进度，这简直令人惊讶。

 [https://www.youtube.com/embed/vsTTXYxydOE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vsTTXYxydOE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

