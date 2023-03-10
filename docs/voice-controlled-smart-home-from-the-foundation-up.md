# 语音控制智能家居从基础开始

> 原文：<https://hackaday.com/2021/08/16/voice-controlled-smart-home-from-the-foundation-up/>

智能家居正在成为一种越来越受欢迎的自动化家居方式，无论是开灯、关百叶窗，甚至是喂养宠物。但是，商业产品通常依赖互联网连接来访问服务器以便工作，这给我们中的大部分人带来了很多隐私问题，并且在互联网关闭时也很不方便。基本上，拥有一个尊重隐私、自给自足的智能家居的唯一方法是从头开始自己建造一个，[这正是【Xasin】在这个项目](https://hackaday.io/project/178551-the-dragons-home)中所做的。

这个构建基于 ESP32 模块，以 Raspberry Pi 为中心，但它不像 MQTT 实现那样简单。不仅自含式家庭自动化设置不依赖于任何外部服务，而且中央 Pi 服务器的故障也不会影响节点，因为它们被配置为即使没有中央控制也能继续独立操作。这允许在没有单点故障的情况下实现强大的家庭自动化，并且还包括一些其他有用的功能，包括语音控制，同时保留了使其相对容易构建的核心设计理念。

该版本不仅在技术上令人印象深刻，因为它的独立功能和消除了隐私问题，而且[Xasin]在物理设计上也做得很好，添加了大量的 RGB 和六边形外壳，无论放在哪里都具有独特的外观。如果你现在正在租房子，或者无法将任何自动化与你现在的家连接起来，一定要看看一些做[家庭自动化而不做任何永久改变的项目](https://hackaday.com/2020/02/09/rental-home-thermostat-gets-smart-upgrade-without-modifying-the-dumb-controller/)。

 [https://www.youtube.com/embed/d9BkHAvRA7Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/d9BkHAvRA7Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

