# 了解椭圆曲线加密和嵌入式安全性

> 原文：<https://hackaday.com/2019/07/04/understanding-elliptic-curve-cryptography-and-embedded-security/>

我们都知道关于“物联网”中的“S”代表“安全”的常见笑话。嵌入式联网设备(“物联网设备”)的安全性往往是最后一分钟的任务，留给了那天不幸第一个走进办公室的实习生，这几乎不是什么秘密。受这种情况的启发，All About Circuits 正在发布一系列关于嵌入式安全的文章，其中重点关注网络安全。

除了初级文章之外，到目前为止，他们已经介绍了 Diffie-Hellman 交换(使用质数、指数和模运算)和使用 T2 椭圆曲线加密(防止任何人暴力破解密钥)的这种交换的发展。当然，不包括任何量子计算机。这三篇文章都应该是任何人都可以理解的，有一个简单的，一步一步的格式。

接下来的文章将专门讨论在微控制器上实现安全性。对于那些迫不及待想了解更多信息的人来说，维基百科上有许多关于[椭圆曲线加密](https://en.wikipedia.org/wiki/Elliptic-curve_cryptography)(将其与更古老且仍然非常常见的 [RSA](https://en.wikipedia.org/wiki/RSA_%28cryptosystem%29) 加密进行比较)的文章，以及在 All About Circuits 文章中讨论的[椭圆曲线 Diffie-Hellman](https://en.wikipedia.org/wiki/Elliptic_Curve_Diffie%E2%80%93Hellman) 密钥协商协议。

这里需要注意的一个细节是，安全通信中最困难的问题不是保持通信继续，而是首先要安全地交换密钥。这就是为什么使用[非对称](https://en.wikipedia.org/wiki/Public-key_cryptography)(或公钥)加密方案的计算成本高得多的密钥交换方案通常用于建立通信的第二部分，这将使用更快的[对称密钥加密](https://en.wikipedia.org/wiki/Symmetric-key_algorithm)方案，其中双方都有办法使用相同的私钥解码和编码消息。

抛开所有的数学问题，人们确实想知道如何表示“安全的”物联网。不知为什么“SIoT”听起来不太上口。