# 逆风飞行:驾驶无电池太阳能遥控飞机几乎就像航海一样

> 原文：<https://hackaday.com/2019/10/07/tacking-against-the-sun-flying-a-batteryless-solar-rc-plane-is-almost-like-sailing/>

依靠太阳能飞行肯定不是一个新想法，但它通常涉及太阳能电池板和推进系统之间的电池。【ukanduit】决定完全失去电池，[用太阳能电池板](https://www.rcgroups.com/forums/showthread.php?3007750-BNF-SolarBear-pure-solar-powered-32-wing-Free-plans)的输出来控制电机的速度。这导致了一些有趣的飞行特征，几乎类似于航海。

当一个负载试图汲取超过太阳能电池板所能提供的电流时，它的输出会急剧下降，所以[ukanduit]必须考虑到这一点。使用 ATTiny85，他建造了一个 MPPT (M 最大功率点跟踪器 )单元，连接 RC 接收器和电机速度控制器。它[监控面板的输出，并相应地调节电机的速度，](https://www.rcgroups.com/forums/showthread.php?3249891-ukanduit-MPPT-for-Solar-powered-aircraft)同时确保始终有足够的电力来运行伺服系统和接收器。机身(名为太阳能熊)是一个小型轻型飞翼，由轻木和碳纤维框架覆盖着透明薄膜，太阳能电池位于机翼内部。由于发动机的推力与有多少阳光照射到机翼顶部成正比，它要求飞行员逆着太阳“前进”，并在再次面向太阳之前利用动量快速转弯。

如果你想建立自己的控制器，原理图和软件是在钢筋混凝土组。看看行动中的太阳熊，由[AJWoods]飞到这里。

 [https://www.youtube.com/embed/kCgWl_TCJac?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kCgWl_TCJac?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们之前报道过[太阳能飞机进入 Hackaday 奖](https://hackaday.com/2016/05/10/solar-fpv-plane-flies-forever/)以及一艘真正的航海[太阳能无人驾驶帆船](https://hackaday.com/2018/09/07/unmanned-sailboat-traverses-the-north-atlantic/)穿越北大西洋。