# 使用 Ghidra 提取路由器配置加密密钥

> 原文：<https://hackaday.com/2021/07/15/using-ghidra-to-extract-a-router-configuration-encryption-key/>

谁不知道奋斗？为一首歌和一支舞购买了一个有趣的硬件，然后发现设备的固件和/或配置文件被各种加密或混淆方法锁定。这就是[阿里·拉希姆]花 18 英镑买下[TP-Link TL-Mr 3020 V3](https://www.tp-link.com/uk/home-networking/3g-4g-router/tl-mr3020/)时的经历，他打算用这种 4G 路由器来提高互联网的可靠性。

当然，这一切都可以在供应商提供的标记线内完成，在这种情况下，这意味着忽略加密的配置文件。作为硬件的所有者，这当然是不可接受的，因此[Ali]从 TP-Link 站点获得了一个固件映像，看看可以从它那里收集到什么加密密钥和其他提示。

在获得 TP-Link 提供的 BIN 文件后， [binwalk](https://github.com/ReFirmLabs/binwalk) 的应用程序帮助提取了嵌入其中的文件，随后[开膛手约翰](https://www.openwall.com/john/)解密了`/etc/passwd.bak`文件中的密码，最终找到了加密的`/etc/default_config.xml`文件。在剩余的提取文件中搜索这个文件名字符串会导致`/lib/libcmm.so`。

将这个共享库文件放入 [Ghidra](https://github.com/NationalSecurityAgency/ghidra) 来反汇编它的代码，【阿里】发现了一个可疑的名为`decryptFile`的函数。里面是一个对全局密钥字符串的引用，当它被扔进 OpenSSL 中，经过一些修改后，结果是以`des-ecdb`模式解密 XML 配置文件。从这一点来看，在加密自己的配置文件以使固件满意后，放入它们应该没有问题。干得好！