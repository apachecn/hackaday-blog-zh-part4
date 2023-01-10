# 研究人员使用可穿戴设备实时检测和逆转阿片类药物过量

> 原文：<https://hackaday.com/2021/12/04/researchers-use-wearable-to-detect-and-reverse-opioid-overdoses-in-real-time/>

不幸的是，在过去几十年中，阿片类药物过量相关的死亡一直在增加，新冠肺炎疫情甚至进一步加剧了这一公共卫生危机。因此，许多科学家、医疗专业人员和政府官员一直在不知疲倦地工作，以结束这一致命的流行病。华盛顿大学的研究人员就是这样一个群体，他们最近推出了一种可穿戴设备，既可以检测阿片类药物过量，又可以实时提供解毒剂，恢复正常的身体功能。

正如研究人员在他们的论文中描述的那样，阿片类药物过量会导致呼吸频率下降，从而导致缺氧(血液中氧气不足)并最终死亡。幸运的是，阿片类药物过量可以很容易地用纳洛酮逆转，纳洛酮是一种与大脑中的受体结合的化合物，胜过阿片类药物本身，并恢复正常呼吸。不幸的是，如果有人用药过量，他们就不能自己给药解毒剂，并且许多阿片类药物过量是在受害者独自一人时发生的(51.8%)，因此有必要开发一种在检测到用药过量时输送解毒剂的自动化系统。

研究人员首先描述了他们测量呼吸的过程，其中有几个选项。你可以使用[光电容积描记法](https://hackaday.com/2020/07/11/detect-covid-19-symptoms-using-wearable-device-and-ai/)，就像我们测量心率一样。或者你可以测量呼吸过程中胸腔阻抗的变化或者甚至使用测量口腔气流的[口内传感器](https://hackaday.com/2018/05/13/intra-oral-device-detects-opioid-overdose/)。相反，研究人员选择通过将加速度计连接到患者的腹部并测量呼吸期间腹腔的运动来测量呼吸。他们承认，当患者不稳定时，他们的技术会有问题，但他们认为，在药物过量的情况下，患者可能会被固定，该设备将能够轻松地测量呼吸。他们在几十名健康的志愿者身上测试了他们的设备，甚至一些鸦片使用者自己，并显示他们的技术与放置在志愿者胸部的参考呼吸带有很好的一致性。

这篇论文的酷之处在于，他们展示了一个“闭环”反馈系统，其中他们的设备测量呼吸，检测呼吸停止(表明用药过量)，并提供解毒剂。为了输送纳洛酮，他们利用了现有的商业药物输送系统，该系统需要用户通过按下按钮来手动激活设备。他们对该设备进行了一点黑客攻击，以便在检测到阿片类药物过量时，可以使用正确定位的伺服电机来启动触发器，从而按下按钮。他们通过要求健康的志愿者屏住呼吸超过 15 秒来模拟药物过量。他们能够成功地向 100%的志愿者群体提供解毒剂，这表明该设备可能在现实世界中发挥作用。

现在，该设备的外形无疑需要改进，以便将该设备部署到现场，但我们认为这些改进正在进行中，并且[患者已经表示愿意佩戴这种设备](https://ascpjournal.biomedcentral.com/articles/10.1186/s13722-019-0153-5)。此外，由于[一些药物过量导致癫痫](https://doi.org/10.1016/0735-6757(94)90185-6)，基于加速度计的呼吸检测是否是最佳选择仍有一点疑问。尽管如此，这是与阿片类药物过量相关死亡的惊人增长作斗争的重要一步，我们希望在这一领域看到病人监测技术的更多进步。