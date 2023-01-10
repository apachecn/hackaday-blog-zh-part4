# OpenISA 推出免费的 RISC-V VEGAboard

> 原文：<https://hackaday.com/2019/02/04/openisa-launches-free-risc-v-vegaboard/>

RISC 架构将会改变一切，我仍然不知道我们是否讽刺地喜欢那部电影。然而，RISC-V 芯片正在进入市场，芯片制造商似乎真的对不支付许可费感兴趣，新的硬盘驱动器正在与 RISC-V 内核一起发运。开放指令集芯片的最新发展来自 OpenISA。他们开发了 VEGAboard ，这是一款带有两个 RISC-V 芯片和 Arduino 风格引脚的开发板。

VEGAboard 装载了恩智浦芯片，该芯片结合了 ARM Cortex-M0 和 Cortex-M4。到目前为止，一切都很好，但是已经有几十种板将两个 ARM 微控制器结合在一个开发平台上。真正的诀窍是 VEGAboard 上的 RI5CY 和 Zero-RI5CY 芯片，这是一个 4 级 RISC-V RV 32 IMC xpulp CPU。[这来自于纸浆平台](http://iis-projects.ee.ethz.ch/index.php/PULP)，这是一个小型、低功耗的并行平台，可满足各种处理需求。简而言之，有了 VEGAboard，您就不用在 RISC-V 微控制器上运行 blink()草图了。您在 ARM 微控制器上运行 blink()草图，同时使用 RISC-V 芯片读取加速度计和切换引脚。是协处理器，但是是 RISC-V。

VEGAboard 的其他功能包括 4MB 的闪光灯、光传感器、加速度计、磁力计、RGB LED、OpenSDA 串行调试适配器、板载 BLE 无线电，当然还有那些不可靠的 Arduino 引脚接头。

现在有，或者曾经有免费的素食者，但是那些已经在 T2 消失很久了。不过，这仍然是一个有趣的平台，如果你想得到一个，生产将很快恢复。当然，如果你现在需要 RISC-V，那么[已经有了真正的 RISC-V Arduinos](https://hackaday.com/2017/01/05/hands-on-with-the-first-open-source-microcontroller/) ，一个带有内置神经网络的 RISC-V [，SiFive 也将很快有](https://hackaday.com/2018/10/08/new-part-day-the-risc-v-chip-with-built-in-neural-networks/)[一个支持 Linux 的 RISC-V 多核板](https://hackaday.com/2018/02/03/sifive-introduces-risc-v-linux-capable-multicore-processor/)。这是激动人心的时刻，每天我们都看到 RISC 架构将如何改变一切。