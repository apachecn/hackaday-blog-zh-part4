# 一架没有所有线路的可破解无人机

> 原文：<https://hackaday.com/2020/05/02/a-hackable-drone-without-all-the-wiring/>

无人机在过去十年里已经走过了漫长的道路，许多使其成为主流的开创性工作都是由个人黑客和小团队完成的。这通常包括将元件拼凑成飞行的乌鸦巢状线路。为了简化黑客的工作，Luminous Bees 的团队正在开发一款从头开始设计的用于黑客攻击的小型 3 英寸无人机。

Ardubee 是围绕一个单独的 PCB 构建的，该 PCB 也充当无人机的框架。板载有一个 STM32F427 微控制器、IMU、气压计和指南针、ESCs、用于遥测的 ESP8266 和一个朝下的测距仪。它可以连接到 SBUS 遥控接收器，一系列可插拔模块正在开发中，以扩展无人机的功能。它的设计是为了运行开源的 Ardupilot 软件，我们已经在这么多 DIY 自动驾驶汽车中看到了这种软件。动力由单个 18650 提供，这可能会限制更高速度的机动性，但对于这种无人机可能用于的更慢的精确飞行来说应该是好的。

该团队已经有了一批为灯光秀开发的更大的 5 英寸无人机。在此过程中，他们开发了自己的超宽带室内定位系统，该系统也将用于 Ardubee。他们希望很快启动 Kickstarter 活动，并向社区征求意见，这样他们就可以知道哪些功能需要优先考虑。我们期待看到这个项目走向何方！

对于 [air](https://hackaday.com/2019/11/06/tiny-drones-navigate-like-real-bugs/) 、 [land](https://hackaday.com/2020/03/15/rover-runs-slow-and-steady-on-solar-power/) 和 [water](https://hackaday.com/2019/12/21/autonomous-boat-for-awesome-video-hyperlapses/) 来说，自动驾驶汽车是这里的一个热门话题，我们毫不怀疑还会有更多。

谢谢你的提示[安德烈亚斯]！