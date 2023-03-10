# 使用 MQTT 在机器间共享剪贴板

> 原文：<https://hackaday.com/2020/08/18/share-your-clipboard-across-machines-using-mqtt/>

我们中的许多人经常从一台计算机转移到另一台计算机，用于工作、娱乐和黑客攻击；时不时地，你会发现自己希望可以在一台机器上复制一些东西，然后粘贴到另一台机器上，中间不需要额外的步骤。[Ayan Pahwa]深知这种挫败感，所以他创建了 [AnywhereDoor](https://github.com/iayanpahwa/anywheredoor) ，这是一个使用 MQTT 的跨平台剪贴板共享实用程序。

一些基于云的解决方案已经存在，但这意味着将你的私人剪贴板数据发送到别人的服务器。Ayan 并不热衷于这个想法，他的解决方案利用了可以在本地网络上任何地方运行的 MQTT 代理，以及可以在 Mac、Windows 和 Linux 上运行的轻量级 python 客户端。客户机以指定的时间间隔检查您的剪贴板，并向代理上的主题发布新数据，所有客户机都订阅了该主题。数据使用 [Fernet](https://asecuritysite.com/encryption/fernet) 对称密钥加密进行端到端加密，因此网络上的其他任何人都无法读取这些数据。目前，AnywhereDoor 仅支持复制文本，但 media 计划在未来版本中推出。

我们喜欢这个实用程序的相对简单性，并且看到它对于在实验室的机器之间跳跃的黑客来说非常方便。解决具体实际问题的简单软件实用程序非常有用，如[布线文档工具](https://hackaday.com/2020/06/23/an-open-source-tool-to-document-your-wiring/)，或 [Kicad 到隔离布线拼接转换器](https://hackaday.com/2020/07/31/transform-kicad-design-to-patchwork-for-isolation-routing/)。