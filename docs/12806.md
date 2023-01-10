# 你好(许多量子)世界

> 原文：<https://hackaday.com/2022/02/17/hello-many-quantum-worlds/>

从历史上看，你为一种新的计算机语言编写的第一个程序是“Hello World”，或者，如果你在德克萨斯州，是“Howdy World”但是随着量子计算的出现，你需要更好的东西。比如《Hello Many Worlds》[IonQ]提出了这看起来像什么，然后用七种不同的量子语言写在一个帖子里，你应该看看。

下面是对这个简单程序的描述:

> 我们要写的基本量子程序很简单。它在两个量子比特之间创建一个完全纠缠的状态，然后测量这个状态。这种状态有时以物理学家约翰·斯图尔特·贝尔的名字命名为钟态或钟对。
> 
> 这个程序的测量结果应该给出等量的两个量子位都是 0 或者两个量子位都是 1。当运行这些时，我们将能够知道我们是在真实的硬件上运行的，因为这并不总是我们所得到的！这些错误是目前限制量子计算机的原因，但是通过量子纠错来克服这些错误的第一步已经开始了。

这些语言包括 IBM 的 Qiskit、微软的 Q#、亚马逊的 Braket、谷歌的 Cirq、苏黎世联邦理工学院的 ProjecctQ、Pennylane、Pytket 和 XACC。如果你想知道学哪一个，看看它们之间的区别是很有趣的。

例如，Braket 看起来很简单:

```

from braket.circuits import Circuit
qc = Circuit().h(0).cnot(control=0, target=1)
print(qc)

```

没有一种语言看起来太复杂，但有时在远程量子计算机上运行它们的设置要多一点代码。如果你想练习的话，其中许多也可以在模拟器上运行。

我们注意到[Twist](https://hackaday.com/2022/02/05/twist-promises-easier-quantum-programming/)——一种相对较新的语言，不在列表中。如果你想对量子有一个温和的[介绍，试试我们的系列。](https://hackaday.com/2018/01/24/quantum-weirdness-in-your-browser/)