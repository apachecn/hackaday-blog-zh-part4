# 用 FPGAs 将微型前视红外镜头变成动作摄像机

> 原文：<https://hackaday.com/2018/09/13/turning-a-tiny-flir-into-an-action-cam-with-fpgas/>

FLIR 目前正在制造一些非常棒的微型热感相机，专为自动驾驶汽车和帮助消防队员安全的工具等应用而设计。这很棒，但这些热感相机太酷了，你真的只想玩一玩。这就是[greg]在设计 PCB 背包时所想的，这种背包可以捕捉来自 FLIR 玻色子的热图像，并将其存储在 SD 卡上。这是一个热动作摄像头，也是一个令人印象深刻的 FPGA 开发。

问题中的前视红外产品是 Boson 640，这是一个令人印象深刻的小相机，以 640×512 的分辨率记录，更新率为 60 赫兹。这款产品拥有 95°视野，规格非常好，尺寸非常小。这是对 FLIR 的 Tau 相机的巨大改进，为此[【Greg】几年前用以太网和 DDR 内存构建了一个分线板](https://hackaday.io/project/160928/log/152588-project-goals-and-motivation-and-background)。一旦他发现了玻色子，他认为这款相机的背包 PCB 是可能的，也是通过动手项目自学 FPGAs 的绝佳借口。

凭借寻找完美器件的非凡能力，[greg]采购了 8×8 mm 封装的 Lattice iCE40 FPGA 和 6×8 封装的 8 Mbit HyperRAM。这种组合允许所有的芯片安装在玻色子相机后面。加上一个 microSD 卡插槽和几个连接器，这款分线板非常接近于一款商业产品，可以满足您可能有的任何前视红外需求。