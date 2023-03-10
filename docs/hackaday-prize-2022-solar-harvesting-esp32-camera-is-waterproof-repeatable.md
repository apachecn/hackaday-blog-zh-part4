# 2022 年 Hackaday 奖:太阳能采集 ESP32 相机防水，可重复

> 原文：<https://hackaday.com/2022/08/14/hackaday-prize-2022-solar-harvesting-esp32-camera-is-waterproof-repeatable/>

[alberto nunez]展示了他设计的光滑的太阳能收集 ESP32 相机——防水，有点节能，几乎任何人都可以建造。为此，他选择了相当软的组件——一个带有匹配原型板的 ESP32-CAM 模块，一个小型太阳能电池，一个 LiFePO4 电池和一个防水的 GoPro 外壳，所有这些部件都可以整齐地放入其中。

BQ25504 能量收集芯片用于确保项目的“太阳能”部分能够为项目的电力预算做出有意义的贡献，否则能量主要由 LiFePo4 电池提供。由于这款电池的标称电压为 3.2 V，它可以直接连接到 ESP32 的电源输入端，不需要调节器——因此，那个被无情地拆焊了。[alberto]还使用 FET 对电路板进行了改造，以控制 ESP32-CAM 模块摄像头的电源，所有这些技术将电路板的深度睡眠电流从 2.8 mA 降至 0.8 mA。对于低功耗设备来说不太好，但对于可以轻松构建的东西来说也不可怕。另外，它防水、防尘，而且非常坚固！

这些 ESP32 相机模块非常漂亮——我们看到它们在常规中得到了很好的利用。无论你是需要在万圣节项目中[检测运动](https://hackaday.com/2021/10/23/esp32-cam-makes-a-dandy-motion-detector/)、[解码你的水表读数、](https://hackaday.com/2021/02/07/an-esp-will-read-your-meter-for-you/)还是仅仅需要一个[安全摄像头](https://hackaday.com/2019/06/10/captivating-esp32-camera-hack/)，在你的工具箱中拥有几个都是值得的。当你在做的时候，也许甚至可以为这些选择一个编程助手。

The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)