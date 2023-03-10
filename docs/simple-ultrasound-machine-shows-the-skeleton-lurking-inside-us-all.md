# 简单的超声波仪器显示出潜伏在我们体内的骨骼

> 原文：<https://hackaday.com/2019/04/18/simple-ultrasound-machine-shows-the-skeleton-lurking-inside-us-all/>

对任何准父母来说，第一次在屏幕上看到子宫中黑白图像的孩子都是一个激动人心的时刻，这是由价值几十万美元的精密医疗仪器实现的。[这台超声波机器是由易贝的零件和模块拼凑而成的](https://www.instructables.com/id/Body-ultrasound-Sonography-With-Arduino/)从长远来看并不是那台机器，但它仍然是一个非常酷的项目，实际上可以窥视皮肤内部。

[stoppi71]在这个建筑中使用的超声波传感器有一个不寻常的来源:一个商业油漆厚度计。暗示看油漆干的笑话，但是涂料测量是严肃的事情。即便如此，这款仪表在易贝上的售价仅为 40 美元左右，为这款产品提供了完美的传感器。发送器需要大约 5 MHz 的 100V 脉冲，因此[stoppi71]用一个升压转换器和一个 74121 施密特触发器单稳态驱动 MOSFET 来切换高压。在接收端，微弱的回波通过使用 AD811 运算放大器的三级放大器发送，然后通过充当整流器和峰值检波器的 LM7171 运算放大器。回声被发送到 Arduino，在 320×480 的 LCD 上显示。分辨率不是很高，但下面的视频显示，足以看到[stoppi71]前臂皮肤和内部骨骼的反射。

[stoppi71]说他是受开源超声项目[Murgen](https://hackaday.io/project/9281-murgen-open-source-ultrasound-imaging)的启发而着手建造的。该项目得到了进一步的完善，并进入了 2018 年 Hackaday 奖的[“最佳产品”类别。我们喜欢这样，因为专注于将项目转化为产品是](https://hackaday.com/2017/07/02/best-product-entry-a-hsdk-for-ultrasound-imaging/)[今年 Hackaday 奖](https://hackaday.com/2019/04/03/2019-hackaday-prize-begins-right-now/)的宗旨。

 [https://www.youtube.com/embed/OyyI-fC30t0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OyyI-fC30t0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

