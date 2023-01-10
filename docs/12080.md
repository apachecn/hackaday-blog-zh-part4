# 3D 印刷电路的秘密成分:电镀

> 原文：<https://hackaday.com/2021/12/06/secret-ingredient-for-3d-printed-circuit-traces-electroplating/>

导电细丝是存在的，但 3D 打印电路板之类的东西需要更多的东西。主要问题是由导电细丝制成的走线基本上是电阻器；它们的行为不像电线。[hobochild]解决这个问题的有趣方法是[用电镀给 3D 打印的轨迹涂上金属](https://www.prusaprinters.org/prints/88763-simple-flashing-printed-circuit)，因此创造了一种 3D 打印电路板。[hobochild]还没有太多的细节可以分享，但他的过程似乎相当清楚。(更新:好消息！[这里是项目页面](https://projectquine.substack.com/p/the-printn-plate-series)和 [GitHub 库](https://github.com/projectquine/electroplating)的更多细节。)

电镀的常见问题是被镀物体需要导电。[hobochild]通过使用两种不同的材料来创建他的测试板来解决这个问题。基层印刷在常规(非导电)塑料中，电路板的超厚走线印刷在导电细丝中。[电镀](https://hackaday.com/2021/01/01/metal-plating-plastic-or-metal-parts/)负责覆盖导电迹线，产生一个非常好看的 3D 印刷电路板，其导体采用真正的金属。[hobochild]使用 Proto-pasta 的[导电灯丝，电路板是一个概念验证的闪烁 LED 电路。鉴于底层材料仍然是塑料，焊接可能是一个挑战，但双材料印刷是一个有趣的角度，甚至允许电镀过孔和通孔。](https://www.proto-pasta.com/pages/conductive-pla)

我们已经看到用于[成功印刷可工作的电连接](https://hackaday.com/2020/08/31/100-printed-flashlight-conductive-filament-and-melted-in-leads/)的导电细丝，但是由于细丝的性质，应用受到限制。电镀是一种几乎每个黑客的工作台都可以使用的技术，它继续以有趣的方式应用于 3D 打印，并且可能是绕过这些限制的一种方式。