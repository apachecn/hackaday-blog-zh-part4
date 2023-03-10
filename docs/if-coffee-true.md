# If Coffee == True {

> 原文：<https://hackaday.com/2020/03/07/if-coffee-true/>

在工作场所拥有一台共享的咖啡机是福也是祸。经常喝咖啡很好，但是当你走进休息室的时候发现咖啡壶已经空了，这很令人沮丧。为了解决他们办公室的这个问题，[Vitort]和公司[建立了一个 IOT 解决方案，在空闲频道](https://vitormelon.com.br/en/2020/03/04/boacompra-coffee-iot-that-tells-you-if-theres-coffee-or-not-in-a-slack-channel-using-esp-8266-and-aws-lambda/)上通知每个人当前的咖啡状态。

这个项目也不仅仅是为了方便办公室而建造的。它大量使用 AWS SNS，Amazon Web Services 的简单通知系统，因为他们想专门学习使用这项技术。除了通知系统之外，该设备本身基于 NodeMCU/ESP8266，通过 WiFi 进行通信，并且是一种简单的按钮设计，当新壶沏好时，咖啡饮用者按一下按钮，当咖啡空了时，再按一下按钮。

虽然相对简单，但如果您对 AWS 感兴趣，尤其是对简单的通知系统感兴趣，这个项目是一个很好的选择。这是一个非常通用的工具，项目中使用的所有代码都可以在项目页面上找到，以供您阅读。如果你对这个项目的咖啡方面更感兴趣，[我们也为你准备了一台特殊的咖啡机](https://hackaday.com/2019/04/26/make-that-special-cup-of-coffee-by-completely-tweaking-the-coffee-machine/)。