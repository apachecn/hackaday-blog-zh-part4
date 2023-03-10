# 新零件日:ST 的新 3D 打印机电机驱动器

> 原文：<https://hackaday.com/2018/10/29/new-part-day-sts-new-3d-printer-motor-driver/>

ST 发布了用于步进电机驱动器的新评估板[。它将直接插入您的 3D 打印机，如果您正在寻找一个芯片来构建一个廉价的 3D 打印机控制器板，这可能是一个。](https://www.st.com/en/evaluation-tools/evalsp820-xs.html)

短短几年内，我们在步进电机驱动器领域取得了长足的进步。RepRap electronics [的第一个受欢迎的驱动器是' *the Pololu'*](https://www.pololu.com/product/1182) ，这是一个使用 Allegro 的 A4988 驱动器的步进电机载板。如果你有一个大散热器，这个驱动器可以为每个线圈提供 2 A 电流，工作电压在 8 到 35 V 之间，微步分辨率低至 1/16。它是周围最好的步进驱动器吗？不，但它很便宜，它无处不在，RAMPS，流行的 RepRap 控制电子产品采用了它的引脚排列，并意外地创建了一个标准。TI 的 [DRV8825 电机驱动器紧随其后，微步降至 1/32，每线圈电流略高，散热设计也更好。](http://www.ti.com/product/DRV8825)

[然后三 mic 驱动的那一波就发生了](https://hackaday.com/2015/01/24/new-part-day-silent-stepper-motors/)。Trinamic TMC2100 是一款静音步进电机驱动器，适用于中速或低速运行的电机。有了这个驱动器，你可以更有效地运行电机，这意味着电机不会变得很热。通过 SPI 进行诊断。[汤姆喜欢它](https://www.youtube.com/watch?v=g6Bxoqr8QlY)，现在在每辆 Prusa i3 中，你会发现一群 Trinamic 驱动程序。

ST 的新产品 STSPIN820 没有 tri amic 驱动器的花哨功能，但芯片本身非常便宜，价格约为 tri amic 驱动器的五分之一。就功能集而言，您可能应该将这款新芯片视为 A4988 的升级版，具有更高的微步距和略高的电流处理能力。

如果您想试用评估模块，可以从 ST 分销商那里获得一个；在撰写本文时，这些模块在全球范围内已经有*17*个。如果你只是想玩 STSPIN820 电机驱动芯片，Mouser 和 Digikey 之间有一万个，第一个数量为 2.97 美元。如果有人能告诉电子制造商一次制造十几个评估板，那就太好了。