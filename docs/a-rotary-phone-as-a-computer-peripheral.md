# 作为计算机外围设备的旋转式电话

> 原文：<https://hackaday.com/2021/11/26/a-rotary-phone-as-a-computer-peripheral/>

对于任何使用复古硬件的人来说，这都是一个古老的难题:是否保留其原始状态？答案往往取决于一个复杂的组合:该设备在其原始形式下有多稀有、过时或不可用，以及该设备的预期用途是什么。对于需要在婚礼上通过老式拨号电话记录美好祝愿的新奇方法的人来说，它不需要完全是原创的，所以解决方案是将它变成主机的 USB 设备。

原来的电路不见了，进来的是一个 USB 集线器、一个 USB 音频接口和一个 Arduino。原来的耳机就足够了，但是麦克风换成了更现代的。Arduino 将注册底座开关，并为设备下方的一组 LED 可寻址灯供电。

其结果是，手机保留了所有的外观，但作为 PC 外设有了新的生命。我们冒昧地建议，也使用 Arduino 读取拨号并产生 DTMF 音可能会使它成为 VOIP 应用程序的有效外设并完成转换，但这是可以在以后完成的事情。也许[它甚至可以给 GSM 改头换面](https://hackaday.com/2018/04/18/classic-american-dial-phone-gets-a-gsm-makeover/)。