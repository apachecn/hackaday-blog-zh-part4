# 自动热交换减少多色印刷的浪费

> 原文：<https://hackaday.com/2022/07/24/automated-hotend-swapping-for-less-wasteful-multicolor-printing/>

在 FDM 机器上进行多色印刷很难做到完美无缺，而且换色时清洗热端会浪费大量的细丝和材料。为了解决广受欢迎的 Prusa i3 和 Ender 3 打印机的这个问题，[BigBrain3D]开发了 [Swapper3D](https://www.kickstarter.com/projects/bigbrain3d/swapper3d) ，这是一个自动系统，当材料改变时，它可以交换整个 hotend，几乎完全消除了清洗的需要。休息后的视频。

Swapper3D 的工作原理与 CNC 机床上的换刀系统非常相似，看起来同样令人满意。机器侧面的一个大型圆形传送带最多可容纳 25 个 hotend，实际上，一对机械臂会弹出前一个 hotend，切割细丝，并从传送带上装载指定的 hotend。这意味着你可以为每种颜色或类型的灯丝单独加热。由于大多数现有的 hotends 也集成了加热元件，[BigBrain3D]创建了一种特殊的 hotend 组件，可以自动移除/插入加热块。

Swapper3D 设计用于现有的灯丝转换器，如 Prusa MMU 和 Mosaic Palette。使用这些系统需要进行大量的清洗，有时在清洗过程中会使用比实际零件所需更多的灯丝。在一个五色演示打印中，Swapper3D 减少了 45%的打印时间和 86%的灯丝使用。它还有助于消除多色印刷中的串线和褪色等问题。凭借这些优势，如果您要进行大量多色打印，看起来 Swapper3D 可能是一个值得的升级，尽管它会给打印机增加相当多的复杂性。

对于更大、更贵的机器来说，更换整个工具架变得越来越流行，甚至 T2·E3D 也加入了竞争。

 [https://www.youtube.com/embed/olXqJadb6BM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/olXqJadb6BM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

