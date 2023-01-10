# 为 DIY 氛围修改灯光

> 原文：<https://hackaday.com/2021/05/23/modifying-lights-for-diy-ambiance/>

几年前，ESP32 和 ESP8266 因其小巧的外形、低廉的价格和无线功能而迅速普及。然而，他们不只是接管了 DIY 的场景。许多大众市场产品也开始整合这些微型芯片，这意味着有一些有趣的预制设备已经成熟，可以进行修改。在这种情况下，[使用非品牌智能灯泡作为半专有照明设置的基础](https://shortn0tes.blogspot.com/2020/03/diyhue-smart-lights-tutorial.html)。

这个建筑中的照明是一个普通的 RGB 灯泡，能够通过 Wi-Fi 控制其颜色。由于它有一个 ESP8266 芯片，它可以通过一些小的修改与飞利浦色调灯一起工作，允许比其他方式更广泛的控制范围。对于这一个，[Vadim]需要撬开灯泡壳才能接触到芯片，然后将电线焊接到芯片上进行重新编程。在这一步中它需要电力，这意味着将由此产生的一堆电线插回灯座，但在这一步之后，新的编程允许灯泡被远程重新编程。

完成这一步后，普通灯泡就可以放入色调照明系统中了。在这种情况下，[Vadim]使用的是运行在 BeagleBone 上的 [diyHue](https://diyhue.org/) ，这是一个 Hue 模拟器，允许在不需要使用任何云服务的情况下控制灯泡。这是一种相当全面的方式，将许多不同类型和品牌的灯泡添加到一个系统中，避免了任何订阅模式或云服务的使用，[这总是我们可以在](https://hackaday.com/2020/02/29/the-iot-trap/)后面得到的东西。

 [https://www.youtube.com/embed/zdDWSp_IO3k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zdDWSp_IO3k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

