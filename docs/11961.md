# 嘶！这是一个新颖的单边带无线电设计，只有七个晶体管

> 原文：<https://hackaday.com/2021/11/20/pssst-heres-a-novel-ssb-radio-design-with-only-seven-transistors/>

当[皮特·胡利亚诺]坐下来为 20 米(14 MHz)业余无线电波段设计边带收发器时，他避开了构成如此多设计的流行电路。他锐意进取，构建了一个新颖的设计，他称之为[皮特的简单七单边带收发器，简称 PSSST](https://www.n6qw.com/PSSST_20.html) 。

PSSST 如此简单的原因不仅在于其结构，还在于其元件数量少。使用四个 2N2222A 的同一电路用于发射和接收。发射时，额外的三个元件介入，放大麦克风输入并建立输出功率，根据最终使用的输出晶体管，输出功率为 2.5-4 瓦。最棒的是，所有的晶体管价格都不到 10 美元！[Pete]展示了射频混频器和晶体滤波器等无线电元件的购买地点，为新手省去许多麻烦。VFO 和中频频率均由德高望重的 si5351a 提供，由 Arduino 掌舵。

许多简单的收发器旨在演示最低可行的无线电，性能并不是真正的目标。另一方面，PSSST 在 LTSpice 中逐级建模，确保出色的发射音频和良好的接收机性能。请务必查看休息时间下方的演示！

[皮特]煞费苦心地在他的网站上记录了整个项目，VFO 的代码可以通过电子邮件索取。我们感谢对家酿火腿无线电社区的贡献，我们相信这将为世界各地的业余无线电爱好者提供许多夜晚的吸烟享受。

 [https://www.youtube.com/embed/bPsxYDC4j8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bPsxYDC4j8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Nick，G8INE]的提示！