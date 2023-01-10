# 用 ArduPlane 取消垂直稳定器

> 原文：<https://hackaday.com/2021/07/09/eliminate-vertical-stabiliser-with-arduplane/>

飞翼是固定翼 FPV 飞行的流行选择，但它们有一个相当恼人的特点:偏航摇摆。飞行时，飞翼会在偏航轴上摆动，这种左右摇摆的运动可以在飞行员的 FPV 视频中看到。通过分离式方向舵和 ArduPilot 的组合，[Think Flight]消除了机翼摇摆，而没有使用任何垂直稳定器。

偏航摇摆通常发生在使用一对小翼而不是中心线上的大垂直安定面的飞翼上。分离式方向舵，也称为差动扰流板，可以通过独立增加任一机翼上的阻力来进行主动偏航控制。然而，这需要非常快速的校正，而手工校正非常困难，所以这就是 ArduPilot 的用武之地。[Think Flight]将偏航阻尼特性与差动扰流板结合使用，完全消除了垂直安定面和偏航摇摆。这与 B-2 隐形轰炸机上使用的避免雷达反射垂直稳定器的技术相同。[Think Flight]也使用这些蛤壳式扰流板作为升降副翼。

利用 XFLR5 翼型分析软件，[Think Flight]设计建造了一对飞翼来利用这些特性。第一种成功地消除了偏航摇摆，但在滚转轴上表现出一些不稳定性。在仔细观察 XFLR5 的设计后，他发现空气预测气流将在小迎角时从机翼底部表面分离。解决这个问题后，他制作了一个 V2，与 B2 爆炸案的外观非常相似。两架飞机都是用有趣的 CNC 热线切割机从 EPP 泡沫上切割下来的，并用凯夫拉尔层压以增加强度。

ArduPilot 是一个非常强大的开源自动驾驶系统，它一直在不断发展。我们最近看到它被用于一次令人难以置信的 [10 小时 45 分钟的电动遥控飞行](https://hackaday.com/2021/06/27/electric-rc-plane-flies-for-almost-11-hours/)，但它也可以用于 [ekranoplans](https://hackaday.com/2021/05/24/ground-effect-drone-flies-autonomously/) 、[漫游者](https://hackaday.com/2020/03/15/rover-runs-slow-and-steady-on-solar-power/)和[船](https://hackaday.com/2021/03/11/drone-boat-sails-seattle/)。

 [https://www.youtube.com/embed/Q1DGNQJ3BQg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Q1DGNQJ3BQg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/5be-4j0yLyw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5be-4j0yLyw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

