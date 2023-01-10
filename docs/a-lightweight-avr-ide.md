# 一个轻量级的 AVR IDE

> 原文：<https://hackaday.com/2019/02/17/a-lightweight-avr-ide/>

完全有可能在 vim 或 emacs 中编写代码，敲击热键来驱动界面并赋予代码生命。虽然以这种方式工作有它的魅力，但它可能会面对新的编码人员，这甚至是在考虑尝试理解命令行编译器设置之前。新手程序员可能会发现他们在 IDE 的温暖怀抱中更加自在，[和[morrows_end]现在已经为那些使用 AVR 汇编代码的人构建了一个 IDE。](https://github.com/morrowsend/savr-ide)

该 IDE 被称为简单 AVR IDE，简称 savr_ide。[morrows_end]使用 FLTK 小部件库用 C++编程，已经在 Windows XP 上测试过了，但指出它应该也能成功地在 Linux、Unix 甚至 MacOS 上编译。

所有的基本功能都在那里——语法突出显示，以及与 AVRA 汇编程序和编程芯片 AVRDUDE 的集成。这是一个工具，可以使进入汇编代码变得稍微容易一点。对于裸机编码的另一种体验，[查看[Ben Jojo]关于 x86 引导加载程序的讨论。](https://hackaday.com/2018/06/19/calm-down-its-only-assembly-language/)