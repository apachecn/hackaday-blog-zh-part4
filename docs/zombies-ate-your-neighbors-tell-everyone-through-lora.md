# 僵尸吃了你的邻居？通过 LoRa 告诉大家！

> 原文：<https://hackaday.com/2019/12/04/zombies-ate-your-neighbors-tell-everyone-through-lora/>

尽管后启示录僵尸类型很受欢迎，但大多数故事都有相当不现实的成分。除了"不死生物在地球上游荡"这件事。但是书呆子在哪里，所有的防末日的太阳能技术在哪里？或者说，正是这些故事中缺乏技术，才是当初建造它的动机？好吧，也许寻找应对我们现代通信基础设施崩溃的方法并不一定是世界末日。想想自然灾害——例如地震或飓风造成的长期停电。[sudomesh]的人们用他们的[完全开源、离网、太阳能、LoRa 网状网络、*灾难无线电*T3]解决了这个问题。](https://disaster.radio/)

网络本身由单个节点构建而成，包括电池供电的太阳能电池板、LoRa 模块以及用于 WiFi 连接的 ESP8266 或 ESP32。这个想法是通过 WiFi 用你的手机连接到网络，因此消除了任何实际使用网络的额外组件的需要，并使节点通过 LoRa 相互通信。诚然，对于高数据速率，LoRa 可能不是您的最佳选择，但当蜂窝网络不可用时，它是长距离通信的好选择。虽然你可以用[【sudomesh】的 GitHub 页面](https://github.com/sudomesh/disaster-radio)上所有可用的东西自己构建它，但 TTGO ESP32 LoRa 模块也可以。

如果这个想法听起来很熟悉，我们确实在今年早些时候报道了类似的项目，如 [HELPER](https://hackaday.com/2019/03/29/emergency-neighbourhood-communications-courtesy-of-helper/) 和 [Skrypt](https://hackaday.com/2019/07/11/adding-lora-long-range-radio-to-smartphones-and-connected-devices/) ，这表明 LoRa 似乎真的是离网通信的热门选择。但是，我们是否真的关心现代通讯和在混乱时互相帮助，而不仅仅是原始地保护我们自己的生命，这当然是另一个问题。