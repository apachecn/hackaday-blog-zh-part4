# Xilinx FPGAs 的自由臂内核

> 原文：<https://hackaday.com/2018/10/02/free-arm-cores-for-xilinx-fpgas/>

令人惊讶的是， [ARM 免费为 FPGA](https://www.arm.com/company/news/2018/10/arm-expands-design-possibilities-with-free-cortex-m-processors-for-xilinx-fpgas) 开发提供了两个 Cortex-M 内核。

自从[Sophie Wilson]为 Acorn Archimedes 家用计算机设计了第一个 ARM 处理器以来的 30 多年里，该架构已经得到了商业管理，成为了这个星球上最广泛采用的架构之一。从家用电器中的微型嵌入式微控制器到高端手机中的超级强大的 64 位多核巨兽，可以肯定的是，即使你没有意识到，你也会拥有相当多的 ARM 处理器。然而，这些处理器都不是由 ARM 制造的，相反，这家总部位于剑桥的公司将把其内核的知识产权许可给另一家半导体公司，后者将根据他们的规格制造相关设备。ARM 核心许可证需要支付电话号码费用，所以除非你是一家资金雄厚的半导体公司，否则到目前为止你可能不需要申请。

你仍将不得不掏钱来获得像那些智能手机巨头那样的强大芯片的核心，但如果你的品味更适中，只喜欢 M1 皮层或 M3，你可能会很幸运。对于 Xilinx FPGAs 的开发人员来说，他们已经通过他们的 [DesignStart](https://www.arm.com/resources/designstart/designstart-fpga) 计划以零成本扩展了这两个处理器内核的供应。

这是免费的，而不是会让开源爱好者高兴的东西，但对于那些想要在自己的门阵列上旋转 ARM 的实验者来说，这无疑是一个令人着迷的发展。有猜测认为这是对 RISC-V 的回应，但我们怀疑这可能是为了吸引学生或研究生等新手开发人员而进行的局部提升。如果你在工作中已经习惯了在 FPGA 层面使用 ARM IP，那么当电话号码交易出现时，你更有可能站在他们一边。

谢谢[Rik]的提示！