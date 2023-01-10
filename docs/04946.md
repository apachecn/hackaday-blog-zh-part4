# 如何在粒子硬件上运行 ML 应用程序

> 原文：<https://hackaday.com/2019/11/26/how-to-run-ml-applications-on-particle-hardware/>

随着 TensorFlow Lite 在 Google I/O 2019 的发布，可访问的机器学习库不再局限于访问 GPU 的应用。现在，您可以更轻松地在微控制器上运行机器学习算法，从而改善板载推理和计算。

[Brandon Satrom]发布了一个关于如何在粒子设备上运行 TFLite 的演示(在光子、氩、硼和氙上进行测试)，使得用预训练的模型对实时数据进行预测成为可能。虽然在 MCU 上发生的一些更简单的计算需要利用现有的等式来操纵数据(例如，将模拟输入映射到百分比范围)，但许多应用需要理解实时收集的大型复杂传感器数据集。从一个简单的方程中得到精确的结果通常更困难。

目前的方法是在专业硬件上训练 ML 模型，在云基础设施上部署模型，并将回程传感器数据上传到云进行推理。通过在板上运行推理和决策，MCU 可以简单地采取行动，而无需回传任何数据。

他首先为 MCU 执行构建了一个简单的 TGLite 模型，使用均方误差表示损失，使用随机梯度下降进行优化。在样本数据上训练模型后，您可以保存模型并[将其转换为 MCU 的 C 数组](https://github.com/bsatrom/Particle_TensorFlowLite/tree/master/examples/linear_regression#performing-inference-on-particle-devices)。在 MCU 上，您可以加载模型、TFLite 库和操作解析器，以及实例化解释器和张量。从那里，您调用 MCU 上的模型，并看到您的结果！

【感谢 dcschelt 的提示！]