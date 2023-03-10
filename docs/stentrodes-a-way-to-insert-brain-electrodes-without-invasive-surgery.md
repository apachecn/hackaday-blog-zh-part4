# 支架植入术:一种无需侵入性手术即可植入大脑电极的方法

> 原文：<https://hackaday.com/2022/08/04/stentrodes-a-way-to-insert-brain-electrodes-without-invasive-surgery/>

当我们想到使用电极的脑机接口(BCI)时，我们通常会想到在开放式大脑手术中直接放置在大脑上的犹他阵列，或者像 Neuralink 的假设的那样，将薄电极拼接到暴露的大脑中。虽然犹他阵列和 kin 作为一个实用的概念可以追溯到 20 世纪 80 年代，但一个更近的概念叫做[支架电极阵列，旨在消除对侵入性脑部手术的需求。](https://en.wikipedia.org/wiki/Stent-electrode_recording_array)

顾名思义，这种方法使用通过血管插入的[支架](https://en.wikipedia.org/wiki/Stent)，它们在血管中膨胀，从而牢固地放置在大脑内的血管中。由于这些支架中的每一个都具有电极阵列，因此它们可以用于记录附近神经簇中的神经活动，以及通过电刺激诱发活动。

由于支架本身已经普遍用于脑血管，以及这些电极阵列相对良性的性质，人体试验已经在 2018 年获得澳大利亚伦理委员会的批准。尽管对这种方法的可实现分辨率和性能仍有疑虑，但它可能会给数百万患有瘫痪和其他疾病的人带来希望。

## 使用现有基础设施

[![Arteries of the brain. (Credit: MedlinePlus, NIH)](img/5cc58e7958617da7169dd7aacde65ebb.png)](https://hackaday.com/wp-content/uploads/2022/07/arteries_of_the_brain.jpg)

Arteries of the brain. (Credit: MedlinePlus, NIH)

在身体的所有器官中，人类的大脑最依赖于持续的氧气和营养供应来发挥功能和生存，因此有一个非常密集的血管网络，支配着每一个单独的部分。虽然这些血管中的许多对于从颈静脉动脉和静脉开始的诸如脑血管支架的医学介入来说太窄，但是大脑脉管系统的大部分因此是可接近的。

在支架电极的情况下，采用与常规支架类似的方法，即使用导丝通过颈静脉和外部跟踪将装置引导到位，以确保其在展开之前到达合适的位置。在几周的过程中，支架完全锚定在血管内部，在那里它可以几乎无限期地保持以提供机械支撑或任何其他需要的功能。

虽然对于使用支架治疗脑血管疾病来说，毫无疑问你为什么要使用这种方法——因为唯一的目标是在血管内部署支撑支架——但对于应该与大脑神经元互动的电极阵列来说，问题是你为什么要选择这种方法。

[![](img/76d41a0ff1290fd5978aa39e2a663ad5.png)](https://hackaday.com/wp-content/uploads/2021/06/Utah_array_pat5215088_had.jpg)

Utah array drawing from Richard Normann’s patent. This part goes into your brain.

显而易见的答案是，它涉及非侵入性手术，不需要打开颅骨，并发症的风险很小，如脑部炎症和侵入性脑部手术可能导致的其他不利影响。这使得它与标准的犹他(或[微电极](https://en.wikipedia.org/wiki/Microelectrode_array))阵列方法，以及 Neuralink 提出的电极串非常不同。从理论上讲，支架置入术可以在局部麻醉下进行，术后恢复时间基本为零。

虽然这里的好处是显而易见的，但仍然存在的问题是 Stentrodes 的性能与其他电极阵列相比如何，以及 Stentrodes 是否会在血液凝固和类似的心血管问题方面造成长期风险，因为需要在大脑静脉内铺设导线来传导信号。

## 检查研究

关于这些血管内支架电极阵列的首次研究可追溯到 20 世纪 70 年代(Penn 等人，1973 年)，其中 [Soldozy 等人(2020 年)](https://thejns.org/focus/view/journals/neurosurg-focus/49/1/article-pE3.xml?tab_body=fulltext)在*神经外科杂志*上提供了一篇系统的文献综述。正如 [Bower 等人(2013)](https://www.researchgate.net/publication/234123014_Intravenous_Recording_of_Intracranial_Broadband_EEG) 所指出的，对于传统的神经植入物，需要通过钻孔或开颅术(提升部分颅骨)进行经颅手术，这限制了使用颅内植入物的吸引力。

在 Bower 等人的研究中，他们比较了血管内电极和硬膜下电极，发现两者诱发癫痫活动的记录反应相似。在 Opie 等人(2016 年)的概念验证研究中，Stentrode 植入物被用于以 4 mA -6 mA 电流刺激绵羊的部分运动皮层。

[![A: Diagram of a sheep brain showing the motor cortex (red), and somatotopic representations of the hindlimb (yellow), forelimb (green), head and eyes (blue), and facial muscles (purple). B: Contrast-enhanced venogram of a sheep highlighting the cortical vessels. The asterisk indicates the desired location of the stent tip in A and B. Bar = 2 cm. C: Stent-electrode array (Stentrode) inside the 1.04-mm internal diameter delivery catheter prior to deployment. Bar = 1 cm. D: Fully expanded Stentrode. Republished with permission of IOP Publishing, Ltd, from Chronic impedance spectroscopy of an endovascular stent-electrode array: Opie NL, John SE, Rind GS, et al., J Neural Eng 13(4): 046020, 2016.](img/f3a2630bd55f637f210ec35a9003f7d1.png)](https://hackaday.com/wp-content/uploads/2022/07/sheep_brain_sections_venogram_stentrode.jpg)

**A:** Diagram of a sheep brain showing the motor cortex (red), and somatotopic representations of the hindlimb (yellow), forelimb (green), head and eyes (blue), and facial muscles (purple). **B:** Contrast-enhanced venogram of a sheep highlighting the cortical vessels. The asterisk indicates the desired location of the stent tip in A and B. Bar = 2 cm. **C:** Stent-electrode array (Stentrode) inside the 1.04-mm internal diameter delivery catheter prior to deployment. Bar = 1 cm. **D:** Fully expanded Stentrode. Republished with permission of IOP Publishing, Ltd, from Chronic impedance spectroscopy of an endovascular stent-electrode array: Opie NL, John SE, Rind GS, et al., J Neural Eng 13(4): 046020, 2016.

在一项对两只羊的研究中，这两只羊要么只有一个支架电极，要么在大脑半球上有一个支架电极以及硬膜下和硬膜外阵列植入物， [Forsyth 等人(2019)](https://ieeexplore.ieee.org/abstract/document/8717000/) 发现，根据记录的数据确定羊的运动的准确性与只使用支架电极一样好，如果不是更好的话。与 John 等人(2019)进行的类似研究的结果一起，这表明 Stentrodes 可能是一种可行的身体质量指数植入物。

这就留下了在这些血管中运行电线的长期影响问题，特别是在凝血和其他潜在的致命并发症方面。在荟萃分析中，活绵羊受试者的最大研究持续时间为 190 天。在研究结束时，对绵羊实施安乐死，并进行尸检以评估植入物的状态。

所使用的装置由[镍钛诺](https://en.wikipedia.org/wiki/Nickel_titanium)制成，这种材料似乎具有良好的生物相容性，并且在体内观察到可诱导[新生内膜](https://en.wikipedia.org/wiki/Neointima)覆盖，这既可稳定材料，又可将其锚定在血管壁中。这很可能也将防止血栓的形成，尽管在这里需要长期的研究来得出可靠的结论。

## 人体测试对象

[![Stentrode array with transceiver unit. (Credit: Synchron Medical, Inc)](img/5c555935ccd4e65987bd6d482327e3c5.png)](https://hackaday.com/wp-content/uploads/2022/07/synchron_stentrode_array_transmitter.jpg)

Stentrode array with transceiver unit. (Credit: Synchron Medical, Inc)

如前所述，Stentrode 植入物的最小侵入性及其对现有的、批准的医疗设备和技术的适应性已经在人类受试者中进行了测试。销售 Stentrode 的公司 Synchron Medical 目前正在澳大利亚的几个地方进行临床试验。这项研究的目标人群是那些受伤或身体状况不佳的人，他们无法完全使用自己的肢体。

使用 Synchron 所谓的运动神经假体，这些受试者被植入支架，这些支架将记录他们运动皮层的活动，并最终恢复对患者肢体的肌肉控制。该研究于 2022 年 6 月才开始，预计该研究将在 2023 年底之前提供结果，说明这是否是一种可行的治疗方法，适用于患有瘫痪但仍有功能性运动皮层的人。

Synchron 网站提供了更多细节，该网站列出了过去、现在和即将进行的临床试验。刚刚开始的临床试验是在[开关 1](https://clinicaltrials.gov/ct2/show/NCT03834857) 试验之后进行的，该试验证实了该装置在人类受试者中的生物相容性。[指令](https://clinicaltrials.gov/ct2/show/NCT05035823)临床试验看起来与 Switch 2 试验相似，但发生在美国。试验受试者的胸部植入了 Stentrode 装置和收发器单元，与收发器的通信显然是通过蓝牙进行的。

## 没有银弹

与所有脑机接口一样，理解当前技术的局限性仍然很重要。当今和临床试验中使用的大多数大脑活动记录设备的一个主要方面是它们是单向的。例如，他们读取运动皮层的活动，并使用这些数据来解释预期的动作和执行肢体运动。然而，来自被操纵的身体部位的感觉输入并没有被提供回患者的感觉皮层，而是在脊髓或中断开始的任何地方逐渐消失。

这也是当前研究正在解决的问题，但挑战仍然是在计算机系统和生物系统变化无常的本质之间提供一个健壮的接口。理想情况下，我们可以提供运动皮层和肌肉之间的 1:1 映射，并从传感器返回到大脑中处理触摸和其他感觉输入的部分，以恢复完整的生物功能。

然而，令人鼓舞的是，人们正在采用和开发多种不同的、也许是互补的方法。即使我们还没有完美的方法来消除伤害和疾病的破坏，通过持续的努力，我们会找到解决剩余问题的方法。不管最好的解决方案是全电疗法、剩余组织的再生疗法，还是两者的结合，这些疗法提供的生活质量的改善使它们如此值得追求。