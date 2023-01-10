# 旁路攻击暴露了加密货币钱包的漏洞

> 原文：<https://hackaday.com/2019/09/13/side-channel-attack-shows-vulnerabilities-of-cryptocurrency-wallets/>

你的加密钱包里有什么？简单的答案应该是大量的比特币或以太币，以及更多。但是，如果你使用硬件加密货币钱包，你可能也有一个很大的漏洞。

在去年的 35C3 会议上，[Thomas Roth]、[Josh Datko]和[Dmitry Nedospasov]展示了对硬件加密钱包的旁道攻击。有问题的钱包是一个[账本蓝色](https://shop.ledger.com/products/ledger-blue)，一个智能手机大小的设备，似乎已经被制造商停产，但仍然可以在二级市场上买到。这个钱包有一个触摸屏界面来管理你的密码帝国，这也是这些研究人员利用的弱点。

通过使用 HackRF SDR 和一个简单的鞭状天线，他们发现每当按下虚拟键输入 PIN 时，钱包就会以 169 MHz 辐射出一个独特的相对较强的信号。每个突发以独特的 11 位数据模式开始；在逻辑分析仪的帮助下，他们确定每个数据包都包含屏幕上按键图标的位置。

下一步:建立一个训练集。他们使用伺服系统和一些 3D 打印部件组装了一个简单的自动按钮捣碎器，并从 SDR 中捕捉每个按键 100 次的信号。原始数据经过了一些处理，为 TensorFlow 做好了准备，经过训练的网络证明足够准确，足以让任何硬件钱包用户暂停——特别是因为他们用相对简单和隐蔽的设备从两米远的地方捕捉到了数据。

每个锁都包含破解它所需的信息，只需要有动机的攻击者使用正确的工具和知识。我们之前已经讨论过[其他旁道攻击](https://hackaday.com/2018/07/27/screaming-channels-attack-rf-security/)；可悲的是，随着 SDR 和机器学习等技术的快速发展，它们可能只会变得更容易。

[via[RTL-SDR.com](https://www.rtl-sdr.com/using-a-hackrf-sdr-to-sniff-rf-emissions-from-a-crytocurrency-hardware-wallet-and-obtain-the-pin/)