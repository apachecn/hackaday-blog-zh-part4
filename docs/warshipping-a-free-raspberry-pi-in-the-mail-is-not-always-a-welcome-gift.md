# 战争运输:邮寄的免费树莓派并不总是受欢迎的礼物

> 原文：<https://hackaday.com/2019/08/19/warshipping-a-free-raspberry-pi-in-the-mail-is-not-always-a-welcome-gift/>

前沿计算机安全隐藏在秘密之中——在这个世界里，新奇的攻击会突然袭击那些还不知道需要防范什么的人。一旦某些策略在酷孩子的圈子里发挥出来，他们就会被介绍给世界其他地方。一个 IBM red 团队展示了[他们所谓的“战争运输”](https://securityintelligence.com/posts/package-delivery-cybercriminals-at-your-doorstep/):在一个盒子里向你发送一个敌对网络。

担心安全的公司已经学会保护他们的互联网访问入口。巡逻的警卫知道要寻找停在附近或反复绕场的潜在守卫。但是有些人对他们的运输和接收比较松懈，他们是战争运输的理想目标。

绕过互联网防火墙和安全边界，攻击硬件被嵌入运输箱内，并由任何一家公共运营商交付。保安人员可能会骚扰一辆布满天线的货车，但他们会挥手让一辆联邦快递的卡车通过！硬件可以被编程为通过筛选保持休眠状态，等待进入墙壁后进行探测。

该演示描述了实施这种攻击的几种方法。原始硬件并没有什么新奇之处——Raspberry Pi、GPS 接收器、蜂窝调制解调器等都是这些页面上各种项目的标准配置。创造性的部分是软件和它们是如何隐藏的:在包装材料和看起来无害的毛绒玩具中。或者为了持久，它们可以隐藏在一些不显眼的光伏板旁边的壁挂牌匾中。(编者注:什么？没有[国玺](https://hackaday.com/2015/12/08/theremins-bug/)？)

随着这种特殊技术的公开，我们确信其他技术已经在使用，并将在几年后公开。与此同时，我们可以把精力集中在类似技术的更良性的应用上，无论是监视我们的猫还是寻找离 T2 最近的快餐店。硬件也在发展:树莓派实际上看起来相当重量级，一个带有[ESP32 和蜂窝调制解调器](https://hackaday.com/2019/07/09/new-part-day-the-15-esp32-with-cellular/)的紧凑型 PCB 怎么样？

Via [Ars Technica](https://arstechnica.com/information-technology/2019/08/hack-in-the-box-hacking-into-companies-with-warshipping/)