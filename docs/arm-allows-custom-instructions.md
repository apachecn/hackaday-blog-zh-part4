# Arm 允许自定义指令

> 原文：<https://hackaday.com/2019/10/23/arm-allows-custom-instructions/>

我们被 ARM 处理器所包围，ARM 处理器在消费市场，尤其是便携式电子产品市场占据着主导地位。然而，Arm Holdings 从未将其商业模式集中在制造芯片上，而是将其 CPU 授权给制造物理设备的其他人。不过，这有点像走钢丝，因为供应商希望让自己与众不同，而 Arm 希望让产品尽可能相似，以实现库和工具链等东西的可移植性和重用。因此，当 Arm 最近宣布他们将首次允许供应商[开发定制指令](https://developer.arm.com/architectures/instruction-sets/custom-instructions)时，有点令人惊讶。至少在 Armv8-M 架构上是这样。

我们认为像 RISC-V 这样的设计正在蚕食 Arm 的市场份额，这是对此的回应。虽然这是一个大新闻，但它不一定像你想象的那么大，因为 Arm 已经允许其他方法通过特殊的协处理器指令和内存映射加速器来做类似的事情。如果你愿意提供一些联系信息，他们有一份完整的白皮书和一个非常简单的例子。该示例显示了手动优化为 12 条 Arm 指令的群体计数函数。然后，它显示了一个可以完成相同工作的自定义指令。然而，他们没有展示实现，也没有提供任何关于速度提升的时间数据。

人口统计(决定一个单词中有多少个 1)是一个很好的例子，说明这种技术可能会有回报。你有一小段数据可以在几个周期内处理。不过，对于许多其他情况，内存映射或协处理器技术仍然更合适。有了协处理器或加速器，你可以有一个独立的部分与主 CPU 并行工作。

定制指令与正常的 Arm 流水线集成。只有特定的指令格式可以使用，你的代码得到和 ALU 相同的接口。这意味着它可以处理数据，但可能无法轻松地操纵处理器的执行。

有什么好处？通常，定制指令执行某些算法步骤的速度比使用普通指令要快。然而，由于你需要有 Arm 内核的许可，我们不太可能看到终端用户添加指令(请，[证明我们错了](https://hackaday.com/submit-a-tip/))。但是你从制造 Arm 芯片的制造商那里购买的芯片可以添加一些指令，比如“验证 ip 地址”

问题是，你会在你写的代码中使用这些指令吗？这样做可能会将您的软件锁定到特定的处理器家族。也就是说，Microchip 不太可能支持 ST 的自定义指令，反之亦然。这对厂商来说是好事，但对开发者或 Arm 来说就不那么好了。在我们看来，这是一个挑战。新的指令将需要有说服力和快速。开发人员不会仅仅为了偶尔在一条指令中做一些愚蠢的事情而限制他们的芯片选择。大多数情况下，你会使用 C 库，你不会关心操作使用了多少指令。

为了获得任何吸引力，供应商需要找到一种不可抗拒的需求，以及一种比其他任何方式更快满足这种需求的定制指令。此外，它需要是一个时间问题。

当然，有时候做一些像人口统计这样的事情可以从更智能的算法中获益更多。尤其是 Arm，非常擅长做[换挡](https://hackaday.com/2015/08/28/firmware-factory-bit-fields-vs-shift-and-mask/)。