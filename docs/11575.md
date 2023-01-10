# RISC-V In… Typescript？

> 原文：<https://hackaday.com/2021/10/14/risc-v-in-typescript/>

我们习惯于看到 Verilog 或 VHDL 中的 RISC-V 实现，但[低级 JavaScript] [在 TypeScript](https://www.youtube.com/watch?v=ER7h4ZTe19A) 中有一个。在你认为它仅仅是一个模拟器之前，要知道这个项目依赖于 [gateware-ts](https://github.com/gateware-ts/gateware-ts) ，一种在 TypeScript 和 Verilog 之间的转换。从那里，你实际上可以把 CPU 放在 FPGA 上。你可以看到下面的发布视频，还有一个开发视频，可能还会有更多。

我们不确定是否有很多 FPGA 设计人员愿意转向 TypeScript。但是，如果你对它感到舒适，它可能会打开 FPGA 开发，而不必学习太多的新语言。

当然，最终产品是 Verilog，它通过供应商的工具进行测试。好消息是，这意味着它几乎可以和任何东西一起工作。坏消息是，这是另一个步骤，意味着像错误消息这样的事情可能不会以一种容易理解的方式直接与您的代码相关联。

有很多 Verilog 和 VHDL 的替代品，但它们似乎都没有得到太多的关注。你可能想要将这个实现(随着它的发展)与 SpinalHDL 中的 [RISC-V 进行比较。话说回来，也许只是](https://hackaday.com/2018/12/08/vexrisc-v-exposed/)[学 Verilog](https://hackaday.com/2018/08/06/learn-fpga-fast-with-hackadays-fpga-boot-camp/) 。

 [https://www.youtube.com/embed/ER7h4ZTe19A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ER7h4ZTe19A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/Vat4p2idDOA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Vat4p2idDOA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

