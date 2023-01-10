# 让无人驾驶赛车变得精简和吝啬

> 原文：<https://hackaday.com/2019/05/31/making-autonomous-racing-drones-lean-and-mean/>

最近，荷兰代尔夫特技术大学的 MAVLab(微型飞行器实验室)自豪地宣布，已经制造出一架重量仅为 72 克的自主无人机。最精彩的部分？它被设计用来参加无人机比赛。这意味着，使用单个摄像头和机载处理，这个直径 10 厘米的小无人机必须在避开障碍物的同时导航。

为了实现这个目标，他们拿了一架 [Eachine](https://www.eachine.com/) [垃圾桶无人机](https://www.eachine.com/Eachine-TRASHCAN-75mm-Crazybee-F4-PRO-OSD-2S-Whoop-FPV-Racing-Drone-0803-16000KV-1200TVL-Adjustable-Camera-25-or-200mW-VTX-Swtichable-p-1328.html)，用开源的 [JeVois 智能机器视觉相机](http://jevois.org/)替换了它的相机，用[狗仔队开放无人机](http://wiki.paparazziuav.org/wiki/Main_Page)软件替换了自动驾驶软件。自然，将赛车无人机缩小到这样的尺寸显然是有成本的:与它的老大哥相比，它的传感器质量低，相机质量相对较低，处理能力有限，因此它必须强烈依赖算法来补偿赛车时的漂移和其他故障。

目前，该无人机主要在代尔夫特大学的 *Cyberzoo，*的一个四门赛道上进行测试，它可以以每秒两米的速度悠闲地飞行多圈，使用它的大门检测算法从一个大门到另一个大门。通过使用机器视觉进行闸门检测，无人机可以处理闸门从航线地图上指示的位置移动的情况。

虽然与其他更大的自主竞赛无人机相比，该系统仍远未达到人类控制的竞赛无人机的性能。为了缩小这一差距，MAVLab 的[Christophe De Wagter]提到，他们正在研究改进算法，使其在预测控制和状态估计以及机器视觉方面更好。理想情况下，这些小型无人机应该比现在更加灵活和快速。

点击链接，查看无人机的运行视频。

 [https://www.youtube.com/embed/sOZJt35dIxM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sOZJt35dIxM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

