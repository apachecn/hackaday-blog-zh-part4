# 用于自行车轮胎的无电池压力传感器

> 原文：<https://hackaday.com/2020/12/06/no-battery-pressure-sensors-for-bike-tyres/>

对于骑自行车的人来说，在长途骑行的中途发现轮胎瘪了是一件令人沮丧的事情。维护

![](img/0f6a7d95479ec7a31687111c3a193b9d.png)

While the epoxy does a great job of sealing the PCB to the valve extension, the overmoulding process would likely be key to producing a product with shelf-quality fit and finish. This test run was done with 3D printed ABS moulds.

正确的轮胎气压是良好骑行的关键，无论你是在道路上积累里程还是在山区处理棘手的单行道。[[captmacallister]组装了一个设备，可以轻松地监视您的轮胎。](https://hackaday.io/project/176052-no-battery-nfc-pressure-sensor-for-bike-valves)

该设备由德州仪器(Texas Instruments)的超低功耗微控制器和压力传感器组成。它是为近场通信(NFC)而设置的，旨在由智能手机供电，智能手机向微控制器查询读数。[我们在 2015 年推出了一款原型车](https://hackaday.com/2015/11/07/measuring-tire-pressure-by-cutting-a-hole-in-an-inner-tube/)，它需要将该装置安装在轮胎的内胎中。然而，这需要侵入性的安装，并且由于弯曲损坏了精密的铜线圈天线，这些设备随着时间的推移会磨损。

新的设计由相同的微控制器硬件组成，但安装在一个经过修改的阀门延伸部分，以适应自行车轮胎的充气阀。印刷电路板直接用环氧树脂粘合在阀门延伸部分上，确保空气不会随着时间的推移而泄漏出去。该组件然后在注射成型过程中被包覆成型，以提供进一步的密封和对元件的保护。这将极大地有助于越野山地自行车的应用。

这款新设备为轮胎压力监测提供了一种简单的旋入式解决方案，无需电池，一劳永逸。[capmcallister]目前正在研究生产运行的选项，鉴于简单的设计，我们想象快速生产几百或几千台不会太难。我们可以想象，它还可以与微控制器、NFC 读取器和车把上的显示设置很好地配对，以在需要时提供实时读数。我们热切期待看到这个项目下一步的走向！