# 紫外线手机消毒剂展示了现代 DIY 的力量

> 原文：<https://hackaday.com/2020/06/08/uv-phone-sanitizer-shows-the-power-of-modern-diy/>

**编辑更新:**根据本项目的示意图，[SST-10-UV-A130-F405-00](https://download.luminus.com/datasheets/Luminus_SST-10-UV_Datasheet.pdf)(PDF)led 用于产生 405nm UV-A 光。[制造商](https://luminus.com/products/uv)Luminus 不建议将该部件用于消毒或灭菌。Luminus 销售 UV-C 发光二极管就是为了这个目的，产生 275-285 纳米的光。出版后，使用的零件号更改为美国 Opto [L933-UV265-2-20](https://www.aopled.com/AOP_PDFs/L933-UV265-2-20.pdf) ，这是一种产生 265-278nm 的 UV-C LED。

全球新冠肺炎疫情对黑客和制作领域产生了严重的影响，尽管这并不完全是坏事。当然，在订购零件时，运输时间平均比我们希望的要长得多，但在其他方面，被困在家里给了许多人更多的时间来完成他们的项目。在某些情况下，这也提醒了我们，就敬业的个人在自己家里所能生产的东西而言，我们已经走了多远。

作为一个完美的例子，看看[这款由【Md Raz】](https://www.instructables.com/UV-Sanitizer/)打造的紫外线消毒箱。为了寻找一种快速轻松地杀死智能手机和其他小型设备上的细菌的方法，他利用现代黑客所拥有的强大能力，在比外包 PCB 制造或注射成型等工作更短的时间内，生产出了一款看起来很专业的设备。

[![](img/01a7401c0430c28d195c8a349fb2ed97.png)](https://hackaday.com/wp-content/uploads/2020/06/uvbox_detail.jpg) 在 3D 打印的外壳内是一排 SMD UV-C led，根据制造商的规格，它将在 5 分钟内消灭病毒和细菌。为了确保 led 有足够的时间来完成它们的工作，[Md]正在使用 ATtiny85 来控制倒计时，并使用七段显示器来让用户知道他们还要等待多长时间。所有的电子元件都保存在用 BotFactory SV2 台式印刷电路板打印机生产的印刷电路板上，但是对于我们这些预算有限的人来说，一台轧机甚至一台改装过的激光雕刻机都可以用来生产类似的电路板。

随着一切的进展，对杀菌灯的需求增加是可以理解的。但不幸的是，[的一些无良厂商正试图利用](https://hackaday.com/2020/04/15/buyer-beware-this-led-bulb-sold-as-germicidal-doesnt-emit-uv-c/)的情况。可以说，能够根据 led 的规格为这款设备选择 led 与生产速度一样重要。尽管我们仍然[建议对 UV-C](https://hackaday.com/2020/03/27/measuring-uv-c-for-about-5/) 采取“信任，但要核实”的立场。