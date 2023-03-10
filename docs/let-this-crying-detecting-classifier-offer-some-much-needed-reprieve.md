# 让这个哭泣检测分类器提供一些急需的缓刑

> 原文：<https://hackaday.com/2020/09/15/let-this-crying-detecting-classifier-offer-some-much-needed-reprieve/>

婴儿监听器很酷，但[Ish Ot Jr.]希望他的监听器只传输需要立即关注的声音，并过滤任何非紧急背景噪音。带着这个问题，[他做了一个婴儿监视器，只有当他的孩子在哭的时候才会发出警报。](https://www.hackster.io/ishotjr/babl-a-baby-monitor-powered-by-tinyml-and-edge-impulse-f5045f)

在他的项目中，[Ish]使用了一个 [Arduino Nano 33 BLE Sense](https://hackaday.com/2019/05/19/new-arduino-nano-line-rolls-out-in-four-flavors-at-maker-faire-bay-area/) ，因为它内置了麦克风、用于存储大块数据的大容量 RAM，以及用于稍后与应用程序连接的 BLE 功能。他通过使用 Edge Impulse Studio 的数据采集功能来收集背景噪音，从而开始了他的项目。[Ish]真的强调了 Edge Impulse 真的在为他做所有的工作。他真的只是需要收集一些测试数据，这是他的大部分。运行和测试神经网络所需的工作由 Edge Impulse 负责。听起来很方便，如果你不介意把数据卸载到云的话。

[Ish]最终获得了 86.3%的准确率，他认为这对于第一次尝试来说已经足够好了。为了让他的原型更“完美”，他添加了一些状态 led，为他的分类器提供一些即时的视觉反馈，并通知护理人员。最终，他想添加一些 BLE 支持和推送通知，在他的宝宝需要关注时提醒他。

这些年来，我们已经在 Hackaday 上看到了几个[婴儿监视器项目](https://hackaday.com/2016/07/15/baby-monitor-rebuild-is-also-esp8266-audio-streaming-how-to/)。[【伊什】的项目肯定会是一个不错的补充](https://hackaday.com/2017/01/03/modified-baby-monitor-interrupts-your-groove-in-case-of-emergency/)。