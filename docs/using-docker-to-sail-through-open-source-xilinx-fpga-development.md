# 使用 Docker 畅游开源的 Xilinx FPGA 开发

> 原文：<https://hackaday.com/2021/05/05/using-docker-to-sail-through-open-source-xilinx-fpga-development/>

直到几年前，FPGA 开发还需要使用专有的锁定工具，但在过去几年中，闭源大坝已经决堤，开源 FPGA 工具如 Yosys、SimbiFlow 和 Icestorm 已经大量涌现。为这些令人兴奋的新工具建立一个构建环境仍然是一个相当大的挑战，但是[Carlos Eduardo]已经决定使用 Docker 为 Xilinx FPGAs 建立一个开源工具链。

他的映像只有三个先决条件:Docker、Python 3 和 OpenOCD(用于将定制的位文件加载到 FPGA 中)。构建 Docker 映像并安装所有工具后，[Carlos]将指导您使用 Python、FuseSoc 和 [SymbiFlow](https://hackaday.com/2019/11/01/symbiflow-open-source-fpga-toolchain/) 构建您的第一个开源 Xilinx FPGA 项目。

除了使设置更加容易之外，利用容器还允许在 Linux、Mac 和 Windows(使用 WSL)上构建相同的开发环境，这将使跨不同 OS 工作的团队的生活更加轻松。[Carlos 的] Dockerfile 是独一无二的，因为它支持流行的 Artix-7 系列 FPGA，对于支持时间更长的 Lattice FPGAs，DockerHub 上已经有了现有的 Docker 文件。这比安装供应商的工具链更容易！

如果这让你觉得是时候涉足开源 FPGA 开发了，请查看 t [在 2019 年超级大会](https://hackaday.com/2020/03/06/mithro-runs-down-open-source-fpga-toolchains/)上对开源 FPGA 工具的概述。