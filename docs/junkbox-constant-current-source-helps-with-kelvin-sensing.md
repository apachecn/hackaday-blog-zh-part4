# 垃圾箱恒流源有助于开尔文检测

> 原文：<https://hackaday.com/2018/11/07/junkbox-constant-current-source-helps-with-kelvin-sensing/>

当一个名为“当前源”的 YouTube 频道需要建立一个当前源时，这是不是很讽刺？或者这不是讽刺，实际上只是巧合？

不考虑语言因素，上述频道的所有者[Derek]在他的一天里制作和拆卸了一些当前的源。这些工作大部分是一次性的精密测量，甚至是驱动他描述为一副引发偏头痛的眼镜中的一串发光二极管。谢天谢地，[下面视频中的垃圾盒电流源](https://www.youtube.com/watch?v=9W8Wv_o0HmY)更多地是为前者服务，而不是后者，因为他的目标是使用开尔文夹子测量半导体中非常小的电阻。

电流源采用 24 伏开关电源和流行的 LM317 可调稳压器。通过一个串联电阻将芯片的调整引脚连接到输出端，可以将 317 配置为恒流模式。多匝电位计提供电流调节，尽管对数锥度并不完全适合应用。我们在构建中也发现了一对似乎是光隔离器的器件，但没有原理图，也没有讨论它们的作用。[Derek]在视频末尾展示了用于 0.47ω1%电阻的开尔文测量的最终产品。

我们很高兴看到[德里克]在行动；你可能还记得他早期的视频，关于甲状腺癌治疗后用盖革计数器测量自己的辐射量。希望那已经过去了。

 [https://www.youtube.com/embed/9W8Wv_o0HmY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9W8Wv_o0HmY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

