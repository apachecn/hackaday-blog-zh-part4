# Lattice Semiconductor 瞄准最新 Propel SDK 许可证中的比特流反向工程

> 原文：<https://hackaday.com/2020/06/05/lattice-semiconductor-targets-bitstream-reverse-engineering-in-latest-propel-sdk-license/>

当涉及到软件和硬件开发时，逆向工程的话题是非常有争议的。自从 Lattice Semiconductor 的 iCE40 FPGAs 的配置协议(比特流)在 2015 年通过逆向工程的努力发表以来，开放比特流协议的支持者和 FPGA 制造商之间一直在进行一场无声的战争，Lattice ECP5 的比特流格式在这一点上已经进行了很大程度的逆向工程。

**更新:**这篇文章发表后大约八个小时，晶格半导体[发表声明](https://www.linkedin.com/posts/lattice-semiconductor_lattice-propel-license-activity-6674864964295114752-fe-5/)收回禁止比特流反向工程的 EULA 语。请查看 [Hackaday 关于这个逆转](https://hackaday.com/2020/06/06/lattice-drops-eula-clause-forbidding-fpga-bitstream-reverse-engineering/)的文章。

最近，看起来 Lattice 已经向开源项目开了一枪。最近发现的[对](https://twitter.com/fpga_dave/status/1268497428501725184) [Propel SDK](https://www.latticesemi.com/propel) 的补充，包含了编程和调试 Lattice 设备的工具，特别提到了比特流逆向工程。当在该公司的网站上用帐户登录时，用户必须在下载前同意[Lattice Propel 1.0](http://www.latticesemi.com/view_document?document_id=52956)的 Lattice Propel 许可协议。该文件包括以下语言:

> 特别是，在[…] (3)中没有授予对任何 Lattice Semiconductor Corporation 可编程逻辑器件的比特流格式或其他信令协议进行反向工程的权利。

对于外行来说，这种“比特流”是一种二进制格式，由 FPGA 用来配置其逻辑元件(LEs)，告诉它 FPGA 内部应该形成什么电路。该比特流特定于 FPGA 的每个特定型号，包含关于芯片内部架构和功能的详细信息。这也解释了围绕所述比特流格式的秘密:通过公布它的规范，人们揭示了 Lattice 的竞争对手(Xilinx、Intel、Microchip 等)关于内部工作的许多细节。)可以利用他们的优势。

比特流与针对 Cortex-M 微控制器之类的编译器生成的二进制代码非常不同。固定 ISA(如 ARMv7a、Thumb/Thumb2)隐藏了微控制器的实现细节。如果这些 isa 不存在，而是直接对处理器的底层实现进行编程，这也将揭示 ARM 不愿意分享的许多实现细节。

禁止反向工程的条款可以在 Lattice 条款的其他部分找到，例如其网站的[法律声明部分:](https://www.latticesemi.com/About/LegalNotices.aspx)

> 您可以使用本网站提供的任何软件，前提是您同意受该软件附带的软件许可协议的条款和条件的约束。除非此类软件的许可协议条款明确允许，否则您不得修改、反向工程或反汇编任何软件。

并且 [Lattice Diamond IDE](https://www.latticesemi.com/en/Products/DesignSoftwareAndIP/FPGAandLDS/LatticeDiamond) 许可证(当登录帐户试图下载软件时出示)引用了底层算法和接口技术:

> 2.9.限制:您不得(也不得允许任何其他人):[……](b)对任何许可产品或任何底层算法、用户界面技术或包含在许可产品中的其他思想进行反编译、反向工程或以其他方式试图导出源代码；

但 Propel 许可证似乎是该公司第一次明确提到比特流。

## 法律事务

这一切将我们带回到法庭上最重要的问题:逆向工程是否合法？这个问题的答案是模糊的。在美国法律中，当涉及到互操作性时，逆向工程有一个“合理使用”的例外。这使得为第一台非 IBM PCs 开发非 IBM BIOSes 成为可能，并允许 Samba 项目重新实现专有的 SMB 网络共享协议。

FPGA 的问题在于协议互操作性:比特流是 FPGA 芯片理解的协议。该比特流可以是纯文本，或者可以是加密的，这在高安全性应用的情况下是合乎需要的。显然，通过访问比特流规范，用户将获得创建他们自己的工具来与(购买的)硬件交互的自由。

本质上，归结起来就是这种比特流协议不受版权法或专利法的保护。唯一真正禁止的部分是 FPGA 制造商编写的软件和相关文档，它们受到版权法和 NDAs 的严格保护。这意味着([洁净室](https://en.wikipedia.org/wiki/Clean_room_design))逆向工程是公平的游戏，使其成为大学的热门目标，正如[这篇 2018 年关于逆向工程的论文](https://www.researchgate.net/publication/328257944_Recent_Advances_in_FPGA_Reverse_Engineering)主要是 Xilinx FPGAs 所展示的。

逆向工程比特流的一个常见用途是[开源社区努力构建不需要使用专有软件的 FPGA 工具](https://hackaday.com/2020/03/06/mithro-runs-down-open-source-fpga-toolchains/)。这有助于构建自动化和工具链的可移植性。这些工具已经足够成熟，可以产生有效的比特流，并且有许多硬件产品的例子，如[破冰者](https://github.com/icebreaker-fpga/icebreaker)、 [Fomu](https://tomu.im/fomu.html) 、 [OrangeCrab](https://github.com/gregdavill/OrangeCrab) ，甚至[2019 hack aday super conference 徽章](https://hackaday.com/2019/11/04/gigantic-fpga-in-a-game-boy-form-factor-2019-supercon-badge-is-a-hardware-siren-song/)，所有这些都是围绕建议使用开源工具链的 Lattice FPGAs 构建的。

## 老 EULA 问题

最终用户许可协议(EULA)的有趣之处在于，人们可以在里面写任何自己想写的东西，而且因为没有人会去读那些该死的东西，所以你几乎可以保证找到违反 EULA 的人。对于 EULA 的创造者来说，不那么有趣的是，除非有国家(或地方)法律的支持，否则 EULA 没有什么分量。

回到 Lattice Propel SDK 许可证(EULA)中新措辞的原始问题。人们可能会注意到，它没有说任何关于逆向工程晶格产品是非法的，只是说不允许使用这些(Propel)工具进行逆向工程。一个人基本上还是可以自由使用其他工具的。

这里的核心问题是，一个人是否可以为了特定的目的而禁止使用软件工具。这是一个很难回答的问题。这是有先例的，例如，某些加密工具[不能从美国合法出口](https://en.wikipedia.org/wiki/Export_of_cryptography_from_the_United_States)到某些国家，尽管这里应该再次指出，这是由于政府的法律。

据我所知，说‘你不能使用我们制造的这些工具对我们的产品进行逆向工程’在这个时候没有任何优先权。然而，看看 Lattice Semiconductor 是否愿意在法庭上测试这种新的 EULA 措辞将会非常有趣。