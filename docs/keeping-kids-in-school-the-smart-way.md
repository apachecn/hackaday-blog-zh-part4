# 明智地让孩子留在学校

> 原文：<https://hackaday.com/2019/09/30/keeping-kids-in-school-the-smart-way/>

对于高流量的机构，如学校和电影院，很难跟踪进出的个人，尤其是在没有足够安全的情况下。尤其是对学校来说，记录学生出勤情况并防止学生在中午离开校园可能是一个代价高昂的问题。

![](img/64d392221cda8cb00f403b6567c99d34.png)

突尼斯工程师[Michael Djimeli]、[Darius Koliou]和[Jinette Tankoua]提出的解决方案是制造一个[智能门](https://hackaday.io/project/165607-smart-gate)，只有在指定的安全官员进行检查时才会打开。该设计对他的家乡突尼斯莫纳斯提尔现有的学校十字转门进行了改造，并使用 RFID 卡、生物识别设备和一系列访问控制来确保试图转动十字转门的学生首先得到验证。

智能门使用几种方法进行识别——通过 RFID、指纹、面部识别或读取二维码。外部数据库存储每个用户的数据和他们的交易历史，有效地存储他们的出勤数据。除了将信息转发给管理员，智能大门还会检查用户的信用——他们是否支付了电影院的入场费，或者他们是否被允许作为学生离开学校。

Raspberry Pi 用作卡收集器，通过 WiFi 传递交易数据信息。与此同时，通过生物识别设备和密钥卡的本地识别信息通过蓝牙中继到处理器。还计划开发一个移动应用程序来远程跟踪智能大门的状态。

虽然完整的系统集成尚未公布，但有几张控制箱的照片，显示了第一个智能大门使用的组件。该机械设计在 IUC 杜阿拉喀麦隆大学校园内成功测试(每分钟识别 35-45 名学生)，该项目有望在来年在更多学校重复进行。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)