# 泰斯拉以预先计算好的密钥卡攻击开场

> 原文：<https://hackaday.com/2018/09/13/tesla-opens-with-precomputed-key-fob-attack/>

这种聪明的预计算攻击是由比利时鲁汶大学的一组研究人员开发的。不像以前的[钥匙链攻击](https://hackaday.com/2014/03/17/hacking-rolling-code-keyfobs/)，我们在过去已经报道过，本质上是中继攻击，这个黑客预先计算大量数据，在数据集中寻找冲突，然后打开门。它是这样工作的。

特斯拉选择不设计自己的密钥卡系统，而是授权了一种基于德州仪器 DST40 密码的产品。使用该系统的车辆广播包含该车辆唯一标识符的无线电消息。如果密钥卡在范围内，它将响应广播，启动加密握手。车辆发送一个 40 位的询问信息，遥控门锁发射器用一个 24 位的响应进行回复。

DST40 是支持这种握手的加密密码。遥控钥匙的电路中烧录了一个 40 位的密钥。DST40 接受 40 位挑战，将其与 40 位密钥结合，并产生 24 位响应。这里的缺点是 24 位响应消息不够长。对于每个质询消息，多个键将产生相同的响应。

研究人员意识到，他们可以选择一个单一的挑战值，并记录下哪些键产生了哪些响应。得到的数据结构为 5.4 TB。通过响应消息的组织，可以非常快速地搜索这个庞大的关键字和响应数据库。有了这个，单个响应消息就可以将 40 位密钥缩小到 2^16 可能的密钥。

在这个缩小的密钥空间内，他们可以暴力破解答案。作者指出，一旦密钥空间缩小，Raspberry Pi 3b+可以在两秒钟内计算出密钥卡的秘密密钥。哎哟！

 [https://www.youtube.com/embed/aVlYuPzmJoY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aVlYuPzmJoY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



他们公布了一辆实车的概念验证攻击，值得一看。试图打开汽车的门触发握手尝试，这放弃了汽车的唯一 ID。有了这个 ID，他们就可以足够接近密钥卡来执行两次握手尝试，第一次使用预先计算的挑战，第二次使用随机挑战。这需要不到两秒钟接近目标遥控钥匙。大约 4.5 秒的计算之后，攻击者拥有一个克隆的密钥卡，并且能够将车辆开走。

经由[连线](https://www.wired.com/story/hackers-steal-tesla-model-s-seconds-key-fob/)。