# 通用生物电信号放大器使读取身体信号变得容易

> 原文：<https://hackaday.com/2021/08/26/universal-bio-electrical-signal-amplifier-makes-reading-body-signals-easy/>

人体发出的电信号告诉我们很多关于内部发生的事情。但是，将这些信号放入微控制器并不容易:对于大多数 ADC 来说，电压太小，而且 50 或 60 Hz 的电源频率始终存在，很难察觉细微的变化。在颠倒实验室，[Deepak Kathri]开发了一种通用生物传感器接口，称为[BioAmp EXG 药丸](https://hackaday.io/project/178997-bioamp-exg-pill)，使这一切变得更加容易。

它的名字是指它可以用于几种不同的生物电传感应用: [ECG](https://en.wikipedia.org/wiki/Electrocardiography) 、 [EMG](https://en.wikipedia.org/wiki/Electromyography) 、 [EOG](https://en.wikipedia.org/wiki/Electrooculography) 和 [EEG](https://en.wikipedia.org/wiki/Electroencephalography) ，它们分别处理来自心脏、肌肉、眼睛和大脑的信号。为了实现这种灵活性，电路板具有用于两个或三个电极的连接器，以及用于安装电阻和电容的焊盘，以调整增益和带宽。仪表放大器增强所需信号的强度，同时抑制噪声和干扰。

这种外形便于一端连接电极，另一端连接数据采集系统。它只有 25.4 毫米长，10 毫米宽，应该很容易集成到你能想到的任何类型的生物传感装置中。[Deepak]已经做了几个演示设置，展示了他使用药丸和 Arduino 来测量他的心率,检测[眨眼](https://www.youtube.com/watch?v=Z9e83V1pikY),甚至[使用自己的手臂肌肉控制机器人手臂](https://www.youtube.com/watch?v=PLUnw17LlUI)!

EXG 药丸是早期的纯肌电图项目 T1 的演变。我们以前见过几个伟大的 [ECG](https://hackaday.com/2019/11/08/uecg-a-very-small-wearable-ecg/) 和 [EEG](https://hackaday.com/2018/08/30/turning-a-fitness-tracker-into-an-eeg/) 项目，但这是我们第一次看到一个放大器可以完成所有这些项目。

The [HackadayPrize2021](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)