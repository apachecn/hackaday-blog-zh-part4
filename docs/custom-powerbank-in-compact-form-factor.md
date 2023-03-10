# 紧凑型定制电源组

> 原文：<https://hackaday.com/2020/12/27/custom-powerbank-in-compact-form-factor/>

18650 锂离子电池的广泛可用性和功率密度使其成为从电动汽车到手电筒等一切产品的良好选择。[Theo]需要为他的 FPV 无人机护目镜提供一个新的电源，所以他设计了自己的带有非常紧凑的充电控制器的[电源。![The narrow PCB slips in between the cells](img/cd343bc8dcbc92694d30c7050d0ec347.png)](https://www.flying-rabbit-fpv.com/2019/02/16/dedicated-power-bank-for-fpv/)

虽然[Theo]可以用 RC 电池充电器给电池充电，但他更喜欢带标准 5V 微型 USB 输入的充电器的便利性，并希望电池电量显示能够避免 FPV 护目镜在飞行途中意外死亡。当四个 18650 单元以立方体排列时，单元之间形成 8x8x65 mm 的间隙。在这一领域,[Theo]能够安装带有微型 USB 插孔、1.3 毫米电源插孔、BQ25606 充电控制器、TPS61085 升压转换器和 ATtiny MCU 的定制 PCB，该 MCU 带有用于电池电量反馈的 LED。充电控制器还允许通过 USB 为 5V 设备充电，而升压转换器通过[Theo]的 FPV 护目镜的 1.3 毫米插孔输出 9V。一切都装在一个漂亮紧凑的 3D 打印外壳内。

这个项目并非一帆风顺。在订购和建造 PCB 后，他发现了一些小的 PCB 布局错误，并意识到转换后的升压只能在 9V 时输出 600mA，这对于他更耗电的谷歌来说是不够的。他计划在下一个版本中解决这个问题。

我们已经看到了许多形状和大小的定制电源组，包括一个使用[电动工具电池](https://hackaday.com/2020/10/10/heavy-metal-power-bank-uses-tool-batteries/)(可能也有 18650s 在里面)和一个几乎拥有[你想要的所有输出](https://hackaday.com/2019/06/05/overengineering-the-humble-usb-power-bank/)，包括交流和无线 QI 充电。