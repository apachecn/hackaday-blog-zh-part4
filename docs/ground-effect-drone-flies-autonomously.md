# 地效无人机自主飞行

> 原文：<https://hackaday.com/2021/05/24/ground-effect-drone-flies-autonomously/>

在世界各地的湖泊和海洋中有许多著名的(尽管是虚构的)海怪，但在里海有一只却是真的。苏联在这里制造了第一辆专门利用地面效应的车辆，其中一辆被称为里海怪物，因为它的发现充满了神秘。虽然这些独特的飞机/船只混合动力最终在几架用于军事用途后被放弃，但这种飞机仍然有一些利基用途，甚至可以用作自主无人机的平台。

这个来自[思考飞行]的建筑是从一个简单的泡沫模型开始的，就是这样一个在他车道上的地效飞行器(或“ekranoplan”)。经过几次试飞，该模型已经足够精确，可以安装一个小型螺旋桨和电池。最终版本的螺旋桨位置从后置改为前置，然后又回到后置，每种配置都有不同的优缺点。最终模型包括~~一架运行~~名为 Ardupilot 的自动驾驶程序的 Arudino，在安装了空气速度传感器的情况下，无人机能够在地面效应中保持飞行，并在湖中高速自主导航预编程的航路点。

作为一项冷战时期的技术，由于其有限的使用案例和极窄的飞行公差，军方已经在很大程度上放弃了这项技术，转而采用其他运输方式，地效飞行器作为遥控飞行器相对来说更受欢迎。这个 RC ekranoplan 使用了相同的 Ardupilot 软件，但配有一个激光雷达系统，而不是 GPS，以在其环境中导航。

感谢[TTN]的提示！

 [https://www.youtube.com/embed/_Cq0ffFiJUY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_Cq0ffFiJUY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

