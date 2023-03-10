# 用 OpenSCAD 和 Light 复制高安全性密钥

> 原文：<https://hackaday.com/2019/09/24/copying-high-security-keys-with-openscad-and-light/>

用 3D 打印机复制钥匙的能力当然不是什么新鲜事，但迄今为止，我们只见过这种技术用于相对较低的悬挂水果。打印一把能打开五金店 15 美元的 Kwikset 锁栓的钥匙是一回事，或者打印一把经美国运输安全管理局批准的“锁”是一回事，但高安全性的钥匙是另一回事。这些按键的几何形状要复杂得多，在消费级打印机上复制它们难度太大。或者至少，你会这么认为。

受之前印刷钥匙的启发，[Tiernan]想看看是否可以改进[技术，用于对抗高安全性的 Abloy Protec 锁](https://hackaday.io/project/167726-protec-3d-printing)，这种锁以抵抗传统的物理攻击如撬锁而闻名。不出所料，生成的 STL 超出了普通桌面 FDM 打印机的能力。但是现在有了低于 300 美元的 Anycubic Photon DLP 打印机，就有可能非破坏性地绕过这些备受推崇的锁。

[![](img/57f670719c660368f5dac91de4ff70dc.png)](https://hackaday.com/wp-content/uploads/2019/09/abloy_detail.jpg) 当然，这些密钥太复杂了[无法从一张图片](https://hackaday.com/2015/09/18/dear-tsa-this-is-why-you-shouldnt-post-pictures-of-your-keys-online/)中复制出来，所以你需要手动获得物理密钥并解码。[Tiernan]明智地省略了这一步骤，因此任何希望使用该项目的人都需要对 Abloy Protec 系统有良好的工作知识。希望这能阻止坏人利用这项研究做任何邪恶的事情。

一旦您获得了想要复制的键的解码值，您只需要将它们提供给[Tiernan]开发的 OpenSCAD 库，并在分辨率足够高的打印机上打印结果 STL。一般来说，由树脂基打印生产的零件具有很高的抗拉强度，但非常脆，所以可能不是你想放在昂贵的 Abloy 锁中的那种东西。也就是说，现在有一些“韧性树脂”配方可以生产出至少和热塑性塑料一样坚固的零件。因此，虽然印刷的按键可能不够坚固，不足以满足日常使用，但在紧要关头它们肯定会发挥作用。