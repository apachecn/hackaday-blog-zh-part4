# RP2040 上的 USB 主机–带 PIO

> 原文：<https://hackaday.com/2022/12/28/usb-host-on-rp2040-with-pio/>

来自【Adafruit】的人们正在[展示一个整洁的黑客](https://blog.adafruit.com/2022/12/22/rp2040-programming-an-rp2040-flash-inception/)——RP 2040 上的 USB 主机，使用现在著名的 PIO 外设。[Adafruit]制造了许多 RP2040 板，当然，在将它们交付给客户之前，您必须对它们进行测试。他们一直在使用非常特殊的青少年，在某种程度上，这些变得不明显。基于[sekigon-gonnoc]的工作，并在[Thach]的帮助下，他们已经使他们的 TinyUSB 库支持通过 PIO 的 USB 位绑定，并成功地将他们的测试夹具固件移植到其上！

由[sekigon-gonnoc]制作的基础版[Pico-PIO-USB repo](https://github.com/sekigon-gonnoc/Pico-PIO-USB)展示了一个相当令人印象深刻的事态——支持低速和全速 USB 主机和全速 USB 设备模式，以及[相当多的示例](https://github.com/sekigon-gonnoc/Pico-PIO-USB/tree/main/examples)来帮助您入门。[【Adafruit】的工作](https://github.com/adafruit/Adafruit_TinyUSB_Arduino/)将这些代码集成到他们的 TinyUSB 堆栈中，特别关注 MST(海量存储)特性——因为这是你编程 RP2040 所需要的。当然，他们也提供[一个大容量存储实例](https://github.com/adafruit/Adafruit_TinyUSB_Arduino/tree/master/examples/)来引导！

当制作多块电路板时，测试夹具[非常重要，拥有](https://hackaday.com/2016/08/24/tools-of-the-trade-test-and-programming/)，并且由于 PIO ，RP2040 支持[更多](https://hackaday.com/2022/08/26/bit-banged-ethernet-on-the-raspberry-pi-pico/)和[更多](https://hackaday.com/2022/04/11/need-a-jtag-adapter-use-your-pico/)接口[，这听起来像是下一个生产测试用 PCB 的完美芯片。有了夹具大脑的照顾，你会想看看建立同样重要的机械零件，我们已经涵盖了相当多的方法来解决这个问题——这里有](https://hackaday.com/2021/01/29/a-look-at-the-interesting-rp2040-peripheral-those-pios/)[一个 OpenSCAD 脚本](https://hackaday.com/2016/10/23/openfixture-takes-the-pain-out-of-pogo-pins/)生成激光切割文件的 KiCad 板，或[一个夹具建立了废铜包 FR4](https://hackaday.com/2022/01/07/production-pcb-and-pogo-pins-produce-a-clever-test-jig/) ，和[一个相当广泛的教程](https://hackaday.com/2017/11/19/homemade-test-jig-is-cheaper-than-outsourcing/)关于制作你自己的激光切割夹具。

 [https://www.youtube.com/embed/sjl7aVK2Q2U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sjl7aVK2Q2U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

