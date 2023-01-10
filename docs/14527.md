# PrusaSlicer 现在导入 STEP 文件，这就是为什么这是一件大事

> 原文：<https://hackaday.com/2022/08/17/prusaslicer-now-imports-step-files-heres-why-thats-a-big-deal/>

PrusaSlicer 有一个新功能:可以导入 CAD 模型进行 3D 打印。从 2.5.0-beta1 版本开始， [PrusaSlicer 可以导入 STEP 格式的 3D 模型](https://github.com/prusa3d/PrusaSlicer/releases/tag/version_2.5.0-beta1)。导入的 STEP 文件在导入时被转换为三角形网格(使其更像典型的`.stl`或`.3mf`文件),这意味着切片会像人们通常预期的那样发生。这是一个非常令人兴奋的消息，因为通常不能将 CAD 格式的 3D 模型直接放入切片器中。有了这个改变，人们现在可以将`.stp`或`.step`文件直接拖到 PrusaSlicer 中进行打印。

首先，简单回顾一下。在 3D 模型的世界中，有两种基本类型:网格和 CAD 模型。[两者的工作方式非常不同](https://hackaday.com/2021/04/20/what-to-expect-from-3d-scanning-and-how-to-work-with-it/#more-470246)，尤其是在编辑方面。3D 打印使用`.stl`文件(网格)已经有很长的历史了，但是对这种文件进行工程类型的更改是很困难的。在 CAD 模型中改变螺纹尺寸或安装孔很容易。在 STL 上，它不是。当 STLs 上需要工程类型的变更时，这个[导致了尴尬的变通办法。而 STEP 是一种被 CAD 程序广泛支持的格式，现在可以被 PrusaSlicer 直接理解。](https://hackaday.com/2018/05/16/3d-printering-when-an-stl-file-is-not-quite-right)

也许这将有助于人们更多地共享他们创建的任何模型的 STEP 文件，因为访问 CAD 文件使其他人更容易进行修改，现在 CAD 文件和可打印模型不必是两种独立的格式。虽然实际上没有什么能够阻止人们以 STEP 格式分享他们的 CAD 模型，但这可能会有助于使其更加规范化。

你可能想知道为什么切片器花了这么长时间才得到这样的特性。一个原因是[步长格式难以实现](https://hackaday.com/2018/05/16/3d-printering-when-an-stl-file-is-not-quite-right/#comment-4561016)。首先，STEP 中的实体(定义模型的元素)可以按任何顺序排列，并且它们自己可以自由地引用其他实体，而不管它们中的任何一个可能出现在文件中的“什么地方”。这使得无法按顺序读取和解析 STEP 文件。相比之下，STL 格式的实现几乎是微不足道的。这在一定程度上有助于保持 STL 作为 3D 打印世界运行格式的惯性。

想试试吗？PrusaSlicer 的测试版可以安全地与生产版一起在机器上运行，并且 PrusaSlicer 支持许多其他打印机(不仅仅是 Prusa 机器)，所以如果你好奇的话，[看一下](https://github.com/prusa3d/PrusaSlicer/releases)。