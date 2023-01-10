# 一种高扭矩 3D 打印谐波传动装置

> 原文：<https://hackaday.com/2021/05/24/a-high-torque-3d-printed-harmonic-drive/>

强大、精确、紧凑和廉价的致动器就像独角兽。他们不存在。然而这正是[3DprintedLife]机器人相机臂所需要的，所以他开发了一种定制的 [3D 打印高扭矩应变波齿轮箱](https://www.youtube.com/watch?v=Emvo3bLT-Z4)，由廉价的 NEMA23 步进电机驱动。

[应变波齿轮](https://hackaday.com/2016/12/09/lego-strain-wave-gear-is-easy-on-the-eyes/)，也被称为[谐波传动](https://hackaday.com/2021/04/07/harmonic-drive-uses-compliant-mechanism-to-slim-down/)，在 Hackaday 上并不是一个不寻常的话题。其工作原理是使一个带有旋转椭圆部分的柔性齿形花键变形，该椭圆部分与外花键的内齿啮合。外花键多了几个齿，导致内花键相对于输入端旋转较慢，实现了非常高的传动比。通常，柔性花键相当长，以允许其在一端弯曲，同时在另一端仍具有刚性安装表面。[3DprintedLife]通过创建一个单独的刚性输出样条来解决这个问题，该样条也与柔性样条啮合。

起初，他为柔性花键使用了齿形橡胶带，这被证明有点太灵活，并引入了不必要的反冲。它被替换为 3D 打印的柔性花键，这也允许[3DprintedLife]调整齿廓，以实现最大扭矩处理和最小齿隙。他还创建了一个 20 公斤的称重传感器，Arduino 和铝挤压自动化测试台。这允许在没有人工干预的情况下重复测试每个设计迭代，允许在部件损坏时快速识别和修复设计弱点。最终版本能够重复产生 10 Nm 的输出扭矩，而[3DprintedLife]只能通过将几乎全身重量放在输出臂上来打破它。

所有的部件都是用 PLA 打印的，但是[3DprintedLife]计划未来转向尼龙。机械臂仍处于设计阶段，但我们期待看到它为未来的视频收集 B-roll。

一个相机臂不需要机动化就能很好地工作。[【伊万·米兰达】](https://hackaday.com/2021/05/05/3d-printed-camera-crane-for-the-workshop/)和[【亚历山大·查佩尔】](https://hackaday.com/2020/09/27/diying-a-high-end-camera-arm/)最近为他们的工作室建造了大型相机臂，并且都大量使用了 3D 打印部件。

 [https://www.youtube.com/embed/Emvo3bLT-Z4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Emvo3bLT-Z4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

