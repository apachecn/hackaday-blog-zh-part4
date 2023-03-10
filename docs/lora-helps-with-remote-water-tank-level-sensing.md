# LoRa 有助于远程水箱液位传感

> 原文：<https://hackaday.com/2022/07/07/lora-helps-with-remote-water-tank-level-sensing/>

[伦佐·米西安提]的朋友必须把水箱灌满。问题是，水箱本身在 1.5 公里之外，所以通常不知道它的水位。那里也没有电力供应——无论使用哪种监控解决方案，都必须是低功耗和自给自足的。为了帮助这一点，[伦佐]正在进行一个独立的自动化项目，有一个通过 LoRa 通信的太阳能传感器，以及一个接收水位读数并在需要时为水泵供电的控制器。

[![](img/7146bcc55f8eec099d4c7e868ef9ed93.png)](https://hackaday.com/wp-content/uploads/2022/07/loralevel_detail.jpg) 【伦佐】在提交设计之前，确保使用屏蔽和模块制作每个部件的原型，并且已经编写和测试了传感器和控制器的代码，并创建了 PCB。他还确保在他进行的过程中记录一切——事实上，关于这个项目有整整[七篇博文](https://www.mischianti.org/category/project/lora-wireless-remote-water-tank-and-pump-controller/)，涵盖了这个项目已经完成的[软件](https://www.mischianti.org/2022/05/20/lora-remote-water-level-and-pump-controller-rewal-client-software-3/)、 [PCB](https://www.mischianti.org/2022/06/15/lora-remote-water-level-and-pump-controller-rewal-client-pcb-5/) 和 [3D 设计](https://www.mischianti.org/2022/07/07/lora-remote-water-level-and-pump-controller-rewal-assemble-client-and-3d-printed-case-7/)阶段。

这些工作日志有大量的解释和图片，[伦佐]为初学者展示了各种不同的制造技术和窍门。最近发布了关于 3D 设计和打印传感器外壳的最后一篇博客文章，这可能意味着我们很快就会看到关于该系统正在安装和测试的文章！

[伦佐]从事“错综复杂的工作日志”业务已经有一段时间了。我们之前已经报道过他的 [3D 打印 PCB 工厂](https://hackaday.com/2019/04/05/cnc-your-own-pcbs-with-a-3d-printed-mill/)和 [DIY 阻焊工艺](https://hackaday.com/2019/03/22/create-green-soldermasked-pcbs-with-fritzing/)，最近有人看到[为一台缺少一个网络接口的 3D 打印机添加了一个网络接口](https://hackaday.com/2021/12/31/3d-printering-adding-a-web-interface-where-there-was-none-before/)。至于 LoRa，你可以制造大量的传感器——无论是[邮箱传感器、](https://hackaday.com/2020/02/15/aaa-powered-lora-mailbox-sensor-goes-the-distance/) [防盗报警器、](https://hackaday.com/2022/01/28/long-range-burglar-alarm-relies-on-lora-modules/)还是[手持信使；](https://hackaday.com/2022/05/25/long-distance-text-communication-with-lora/)现在你又多了一个可以从中汲取灵感和知识的项目。[伦佐]之前做了[一个劳拉教程](https://hackaday.com/2020/02/25/lora-tutorials-for-the-diy-masses/)让你开始，我们做了[一个关于劳拉旺的！](https://hackaday.com/2022/01/21/casually-chirping-into-the-world-of-lorawan/)

 [https://www.youtube.com/embed/FZrArEnKOAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FZrArEnKOAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

