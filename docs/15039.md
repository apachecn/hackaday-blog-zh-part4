# 用 Arduino 实现简单的数控齿轮生产

> 原文：<https://hackaday.com/2022/10/10/simple-cnc-gear-production-with-arduino/>

这些年来，我们已经看到很多人 3D 打印定制齿轮，但[创新先生]决定反对为他的定制组件添加工艺。他最终使用了一台简单的数控机床,这台机床使用了几个从 3D 打印机中回收或在一台打印机上生产的部件。使用一个小锯片，机器将齿轮齿切割成一些塑料材料，并且——大概——可以将齿轮切割成锯片能够切割的任何东西，特别是如果你添加一点润滑、冷却和除尘的话。

如果你已经建造了一台 3D 打印机，你会看到许多熟悉的部件。步进电机，铝挤压，直杆，轴承座，和杆持有人都在建设中使用。在打印机的 Z 轴上还有一个丝杠和相关部件。很自然，Arduino 驱动着整个事件。

锯片是由垫圈定制的，打磨边缘，并使用 3D 打印模板在其中切割齿。我们可能更倾向于使用旋转工具上的切割轮，但这确实奏效了。LCD 接受齿轮直径和齿数。步进器旋转正确的度数，另一个步进器降低切割头，切割头用普通的 DC 马达旋转。

尽管这台机器令人印象深刻，但事实是 3D 打印机可以生产更复杂的设计。例如，人字形图案可以帮助解决对齐问题。已经[做了很多次](https://hackaday.com/2021/04/25/7000-rpm-on-a-3d-printed-gearbox/)。你甚至可以使用树脂打印机，尽管你[可能更喜欢用 FDM](https://hackaday.com/2022/02/10/resin-printed-gears-versus-pla-which-is-tougher/) 。

 [https://www.youtube.com/embed/t-kQO8uDfLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/t-kQO8uDfLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

