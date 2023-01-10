# Fortran 变得交互式

> 原文：<https://hackaday.com/2019/05/03/fortran-goes-interactive/>

当你想到 Fortran 时，你可能会想到穿孔卡片和绿色条纸。虽然 Fortran 确实不再是它曾经的首选语言——这是无意的——但它仍然有一个充满活力的社区，里面的人都在认真处理数字。然而，该社区的许多成员已经被同样擅长数字处理的交互式工具所吸引，如 MATLAB、Julian 和带有特殊库的 Python。LFortran 项目的目标是创建一个像 Python 一样具有交互性的 Fortran 环境，但保留 Fortran 众所周知的速度。

最终的工具令人印象深刻。您可以在 Jupyter 中使用它，可以解析针对现有 Fortran 编译器的代码，并且支持 Linux、Mac 和 Windows。有开发使代码与其他语言如 C 或 Python 完全互操作，以及利用 GPU 和其他专门的硬件。他们还瞄准了对 Fortran 2018 的全面支持。

如果你想尝试一下，你可以去 [Git 库](https://gitlab.com/lfortran/lfortran)。然而，由于它与 Jupyter 兼容，你可以使用[活页夹](https://mybinder.org/v2/gl/lfortran%2Fweb%2Flfortran-binder/master?filepath=Demo.ipynb)在线打开它。开发人员希望人们不要把它仅仅看作是运行遗留代码的一种方式，而是要把 Fortran 介绍给新一代的开发人员，他们将用它来做新的事情。

我们已经看到 Fortran 最近有所回归。你可以用它来[提供网页](https://hackaday.com/2016/12/27/fortran-for-the-web/)，尽管这可能不是对其功能的最好利用。如果你想了解更多关于使用支持多种不同语言的 Jupyter 笔记本，我们[在今年早些时候报道过这个](https://hackaday.com/2019/02/22/drops-of-jupyter-notebooks-how-to-keep-notes-in-the-information-age/)。