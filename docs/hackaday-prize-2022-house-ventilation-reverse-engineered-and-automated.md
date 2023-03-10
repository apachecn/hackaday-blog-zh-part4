# 2022 年 Hackaday 奖:房屋通风逆向工程和自动化

> 原文：<https://hackaday.com/2022/06/01/hackaday-prize-2022-house-ventilation-reverse-engineered-and-automated/>

[Marcel]想——如果他能更好地控制房子的通风系统会怎么样？你可以添加一些漂亮的功能，比如在早上大家都不在的时候自动给你的房子通风，只在没人听到的时候制造噪音。可悲的是，大多数通风系统都不是自动化友好的——然而，他很幸运，因为他的系统带有无线遥控器。[Marcel]对这个遥控器进行了逆向工程，[创建了一个使用相同协议的 USB 加密狗](https://hackaday.io/project/184310-fresh-air-automation-by-rf-usb-dongle)，并将其绑定到他的家庭助理设置中！

问题中的遥控器是 Orcon R15，带有一个 Atmel MCU，通过 SPI 与 CC1101 芯片通信。他在按下不同按钮时嗅探 SPI 通信，通过比较记录找出协议，并用备用 Arduino 和 CC1101 模块建立了一个测试设置。这很有效，他开始使用 ATMega32U4 设计一个独立的加密狗。加密狗看起来非常整洁，适合哈蒙德外壳-有什么不喜欢的？

然后他着手开发固件，在这方面也没有让人失望。他的代码不仅在控制方面完美地模仿了原始遥控器，还具有用户友好的配对流程，跟踪系统的当前状态，并仍然让原始遥控器并行使用。PCB 的 Eagle 文件可在项目页面[获得，](https://hackaday.io/project/184310-fresh-air-automation-by-rf-usb-dongle/files)代码和 PDF 原理图可在 GitHub repo[获得。](https://github.com/Marcelh1/orcon-usb-dongle)hack aday . io 页面描述了整个旅程，我们建议您查看它提供的所有见解！

通风系统往往不是为自动化而设计的，看到黑客们致力于征服这一前沿领域令人欣喜。上次我们看到一个通风系统黑客，它有一个对房东友好的额外挑战，我们认为[黑客抓住了它！](https://hackaday.com/2022/03/13/reversible-ventilation-hack-keeps-the-landlord-happy/)

The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)