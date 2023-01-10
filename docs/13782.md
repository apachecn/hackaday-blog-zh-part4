# 过期证书导致德国支付崩溃

> 原文：<https://hackaday.com/2022/05/30/expired-certificate-causes-german-payment-meltdown/>

对于大多数 Hackaday 读者来说，这个周末购买食品杂货的过程相对来说并不痛苦，但是我们猜想我们的一些德国朋友会发现他们的信用卡意外地被拒绝了。原因？一款流行的支付卡终端，Verifone H5000，遭遇了所谓的“软件故障”。那么到底发生了什么？答案既简单又不幸:[存储在设备上的德国交易处理安全证书已经过期](https://twitter.com/jwildeboer/status/1530227390286290944?t=a8tMjoGGLW6fDnujWtpY4Q&s=03)。

整个故事暴露了假设支付终端是一个电器，而不是一台计算机及其相关软件(像其他任何东西一样需要更新)的缺陷。H5000 是一种旧码头，在过去十年中停止生产，已经达到使用寿命，但它仍在使用，更严重的是，它仍在供应链中，供购买码头的商家使用。由于更新需要现场访问而不是空中升级，这种混乱的影响可能会持续一段时间。

如果你对这类设备的硬件感兴趣，[我们在过去曾经拆卸过另一台 Verifone 终端](https://hackaday.com/2019/07/08/teardown-verifone-mx-925ctls-payment-terminal/)。