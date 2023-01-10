# 2022 年 Hackaday 奖:DIY 滑坡预警系统

> 原文：<https://hackaday.com/2022/09/06/hackaday-prize-2022-diy-landslide-warning-system/>

山体滑坡对人和财产都非常危险。和大多数自然灾害一样，预警会带来很大的不同。[[air pocket]已经建立了一个廉价的、负担得起的系统，希望能提供这样的服务。](https://hackaday.io/project/187007-diy-landslide-warning-system)

该系统依赖于一个由索尼 Spresense 控制器构建的传感器网络，内置于太阳能花园灯外壳中，提供防水外壳和可持续的电源。控制器与加速度计配对以检测运动，并通过 WiSUN 连接与 Raspberry Pi 4B 基站通信。当部署的传感器站检测到移动时，它会向基站发回消息，发出滑坡可能即将发生的警报。

早期测试表明这个概念在理论上是可行的。在实践中，需要一些改进来降低功率消耗并增加通信可靠性。然而，对于一个简单的滑坡预警系统来说，这是一个坚实的概念证明。

对于山体滑坡、海啸和地震，早期预警总是至关重要。事实上，美国地质调查局在预测地震和提供早期预警方面也做了自己的工作。休息后的视频。

 [https://www.youtube.com/embed/OrEw94bvgL0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OrEw94bvgL0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)