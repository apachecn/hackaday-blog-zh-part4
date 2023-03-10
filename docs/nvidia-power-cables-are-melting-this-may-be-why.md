# NVIDIA 电源线正在融化，这可能是原因

> 原文：<https://hackaday.com/2022/10/28/nvidia-power-cables-are-melting-this-may-be-why/>

NVIDIA 最近发布了他们的 40 系列显卡阵容，带有名为 12VHPWR 的新一代电源连接器。看，上一代 8 针连接器已经不足以满足 GPU 的需求。一旦卡开始进入用户手中，令人惊讶的是，我们开始在网上看到熔化的 12VHPWR 插头和插座的图片——具体来说，涉及 NVIDIA 随卡提供的 ATX 8 针 GPU 电源到 12VHPWR 适配器。

现在， *igor'sLAB* [的【Igor Wallossek】提出了一个关于正在发生的事情的理论，](https://www.igorslab.de/en/adapter-of-the-gray-analyzed-nvidias-brand-hot-12vhpwr-adapter-with-built-in-breakpoint/)用令人信服的拆卸图片来支持它。在一股散发着塑料气味的魔法烟雾意外释放后，NVIDIA 提供的一个连接器被破坏性地拆卸了。事实证明，这些连接器不像我们习惯的那样卷曲，而是具有扁平的金属焊盘，用于焊接电线。对于带电源的连接器来说，有充分的理由说明这不是标准。也就是说，你可以让它工作，但机会并不支持这个特定的。

有问题的金属焊盘似乎太薄，结构不合理，人们很容易发现，它们的横截面与焊接到其上的电缆的横截面相比相形见绌。这将产生一段增加的阻力和热损失，由于粗而笨重的电缆的任何弯曲而加剧。由于金属非常薄，应力点看起来非常脆弱，因为在拆卸连接器的过程中，其中一个金属垫直接断裂。

如果这个理论是真的，这种情况是英伟达的失误。从好的方面来看，12HPWR 标准本身似乎是可行的，因为有一些具有原生 12 hpwr 连接的 PSU 不会出现这个问题。看起来，拥有顶级 GPU 的游戏玩家现在可以理解我们黑客[在非常便宜的 3D 打印机中看到的问题。](https://hackaday.com/2016/12/07/dont-leave-3d-printers-unattended-they-can-catch-fire/)