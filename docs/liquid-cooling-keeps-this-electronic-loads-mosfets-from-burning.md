# 液体冷却防止这种电子负载的金属氧化物半导体场效应晶体管燃烧

> 原文：<https://hackaday.com/2020/01/07/liquid-cooling-keeps-this-electronic-loads-mosfets-from-burning/>

问题:你的电子负载工作正常，除了偶尔 MOSFET 着火。解决方案:做【tbladykas】做过的事情，[造一个水冷电子负载](https://www.reddit.com/r/electronics/comments/ej4neo/water_cooled_linear_mosfet_electronic_load_for/)。

有人可能会吹毛求疵地说，也许有其他方法来防止你的 MOSFETs 燃烧，包括改变电气设计。但他决定从[凯瑞·王]的设计书中汲取经验，做大。[【Kerry】的电子负载](https://hackaday.com/2017/02/28/beefy-100-amp-electronic-load-uses-two-mosfets/)是风冷的，能够吸收 100 安培电流；只需要 60 或 70 安培左右。因为他手头有一个一体化液体 CPU 冷却器，所以使用它来冷却是很自然的。

IXYS 线性 MOSFET 悬挂在控制器 PCB 的末端，其中 TO-247 器件直接焊接到 AiO 冷却器的铜冷却板上。这可能看起来很粗略，因为如果事情失控，焊料可能会熔化，但是再次钻孔和敲击冷板可能会导致热耦合流体的泄漏。它还没有经过任何严格的测试——他猜测此时的功耗为 300 瓦——但由于他的主要目标是阻止 MOSFET 起火，具体细节并不重要。

我们之前已经见过相当数量的液冷 [Raspberry Pis](https://hackaday.com/2017/05/15/liquid-cooling-overclocked-raspberry-pi-with-style/) 和 [Arduinos](https://hackaday.com/2010/02/16/ultimate-flame-bait-liquid-cooled-arduino/) ，但是我们找不到液冷电子负载的例子。或许[tbladykas]在这个设计上有所发现。