# 铜模有助于冷却炎热的 GPU

> 原文：<https://hackaday.com/2022/03/24/copper-modding-helps-cool-a-toasty-gpu/>

[DandyWorks]有一个 NVIDIA RTX 3070 Ti GPU，发现它运行得非常热，卡的内存达到了 110°c 的温度。他决定尝试“铜调制”来解决这个问题，[并在这个过程中做出了一些令人印象深刻的改进。](https://www.youtube.com/watch?v=f8f6ZHCPVpw)

铜调制是指使用小铜垫片将 GPU 上的热芯片连接到散热器，比制造商使用的标准散热垫更有效。铜的导热性比导热垫好得多，因此以这种方式使用时，有助于改善组件的冷却。

通过仔细拆卸 GPU，[DandyWorks]指出，该设计使用了专门用于内存芯片的次级散热器。然后，他开始用异丙醇移除芯片上的散热垫。它们被精确厚度的铜垫片取代，带有一层薄薄的导热膏以确保良好的热流动。[DandyWorks]还用 Kapton 胶带保护电路板的所有周围部分，以避免铜垫片在任何位置移动时发生短路。

运行相同的哈希操作，GPU 现在可以在更低的温度下运行其内存，温度仅为 64 摄氏度。[DandyWorks]进行了几个小时的测试，温度没有超过这个温度。有证据表明，与普通的散热垫设置相比，铜垫片在将热量传导出内存芯片方面做得更好。

我们以前已经看到过这方面的一些有趣的模式，例如 [CPU 芯片研磨以获得更好的热性能。](https://hackaday.com/2020/07/21/die-lapping-for-better-cpu-performance/)休息后的视频。

 [https://www.youtube.com/embed/f8f6ZHCPVpw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f8f6ZHCPVpw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

