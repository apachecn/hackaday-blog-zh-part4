# 走向低成本生物医学成像

> 原文：<https://hackaday.com/2019/01/07/towards-low-cost-biomedical-imaging/>

医学成像是技术的最佳应用之一——它允许我们在不实际进行手术的情况下窥视人体内部。这是一种极端的非破坏性测试，我们在过去一年中看到的一个更有趣的项目使用交流电流和无限电阻网格来成像活体的内部。它叫做 Spectra，是 Jean Rintoul 的发明。她在 Hackaday 超级会议上的演讲是关于低成本和开源生物医学成像的。

这些年来，我们在 Hackaday 奖中看到了一些有趣的医学成像黑客。已经有了静脉探测器，甚至还有了 CT 扫描仪，但是当涉及到生物医学成像时，[Spectra 项目](https://hackaday.io/project/159737-spectra-open-biomedical-imaging)就不一样了。现在，*只是*足够好，可以在器官还在你体内的时候对它们进行成像，而且还有很大的潜力可以做得更多。让我们仔细看看这是如何工作的。

 [https://www.youtube.com/embed/5kuseBfnvzs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5kuseBfnvzs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Spectra 背后的想法是使用 AC 波通过一种介质(一种水果，或一个人，或一只老鼠)，并使用层析成像技术对内部成像。具体来说，这就是所谓的电阻抗断层成像，你可以用非常非常少的硬件令人惊讶地建造一个小型的这种成像系统。

[![](img/d9649f9fb450f9f38acde8b02a7603ee.png)](https://hackaday.com/wp-content/uploads/2018/11/baby.png)

EIT electrodes on the chest of a 10-day-old baby

电阻抗断层成像的工作原理是不同的组织类型具有不同的电阻。通过发送一个交流波(大约 10kHz 左右)通过一个身体，内部可以被重建。从肺体积测量到肌肉和脂肪质量到癌症的一切都可以用这种技术检测出来。是的，你仍然需要技术人员或医学博士来解释数据，但与目前的技术相比，这是一种非常便宜的人体成像方法。

至于为什么这很重要，这是一种极其廉价的观察身体内部的方法。医学中的预防保健没有负担得起的成像解决方案；如果你需要核磁共振或 CT 扫描，很可能你只有在生病的时候才能得到。一台 CT 扫描仪将花费数百万美元，核磁共振成像设备甚至更贵。[Jean]的原型电子断层扫描装置可以用不到 1000 美元来建造——看起来她甚至有一个众筹活动在进行中,以向世界推出更多的测试硬件。开源和低成本使得这项技术更容易获得。我们希望这最终能为每个人带来更好的医疗保健，而[Jean]正站在这一进步的最前沿。