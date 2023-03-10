# 约翰麦克马斯特解释加密点火电话钥匙，以及如何复制它们

> 原文：<https://hackaday.com/2019/12/02/john-mcmaster-explains-crypto-ignition-phone-keys-and-how-to-reproduce-them/>

当你是一个民族国家，安全的通信是保护你的主权和保密你最好的计划的关键。对于美国来说，这一要求导致了多年来一系列安全电话网络的发展。约翰·麦克马斯特发现自己对研究 STU-III 保密电话的工作方式很感兴趣，并着手复制该系统使用的保密钥匙。

![](img/098ad56bc42fc8d84afb5b7851031876.png)

An encryption key in a very physical, real sense, the Crypto Igntion Key was used with the STU-III to secure phone calls across many US government operations. The key contains a 64KB EEPROM that holds the cryptographic data.

[John]特别喜欢 STU-III 加密电话的方法。必须将一种称为加密点火钥匙的物理设备插入电话，并发出令人满意的沉闷金属声来启动加密。该物理密钥包含数字加密密钥，与电话中的密钥结合使用，用于加密呼叫。触觉界面向用户提供了关于保护通信信道的非常清晰的反馈。约翰希望了解更多，开始进一步研究该系统，并试图寻找一些硬件进行修补。

正如约翰在他的黑客日超级会议讲话中解释的那样，他能够找到一个民用型号的 STU-III 手机，但是钥匙很难找到。作为加密密钥的载体，很可能大多数密钥在到期时都被安全协议销毁了。然而，在他的手放在一个坏掉的钥匙上后，他能够创建一个 CAD 模型，并生产出一个机械兼容的原型，它将适合插槽并正确转动。

 [https://www.youtube.com/embed/bp1hWR8_UvY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bp1hWR8_UvY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



由于密钥的稀有性，破坏性逆向工程并不实用，所以使用了其他方法。由于 STU-III 在军事领域的使用，这些钥匙有一个国家库存编号，指向 AMD 的并行 EEPROMs。有了数据表和来自加密博物馆的加密密钥的 x 光片，就有可能找出密钥的大致轮廓。有了这些信息，电路板被生产出来，并与 EEPROM 和 3D 打印结合起来，生产出可以复制原始功能的钥匙。

![](img/8553b15a519447710a6cfe43dc11ee2f.png)

With the key inserted into the handset and turned, calls could be secured at the touch of the button across standard analog phone lines.

像大多数项目一样，第一次没有成功。印刷的钥匙存在齿的质量和支撑材料的冲洗的问题，通过简单地将它们完全移除并依靠电路板来索引相关的销就可以解决该问题。测试是使用 PKS-703 密钥阅读器进行的，它本身是一种非常罕见的硬件。结合逻辑分析仪，它揭示了一对夫妇的写引脚是向后排列。一旦解决了这个问题，密钥就可以工作了，并且可以用一组加密密钥进行编程。一旦插入 STU-III 并转动，电话就开始工作了！

尽管取得了成功，但在约翰开始用 STU-III 打安全电话之前，还有很长的路要走。只有一部手机，他的能力有限——理想情况下，需要一部手机来做进一步的实验。他还试图让其他人更容易摆弄这种硬件，包括开发一种电路板，允许用标准 EEPROM 写入器读取和重新编程密钥。他还开始了 STU-III 内部的逆向工程。作为一点乐趣，John 甚至复制了 STU-III 项目的一些促销赠品，展示了他未来的安全语音系统杯子和 t 恤。

对国家安全设备进行逆向工程肯定会带来一系列独特的挑战，但约翰已经证明他能够胜任这项任务。我们期待看到密码社区更深入地侵入这个硬件，也迫不及待地想看到黑客们通过古老的 STU-III 打电话！