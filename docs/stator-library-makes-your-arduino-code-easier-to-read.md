# 定子库使你的 Arduino 代码更容易阅读

> 原文：<https://hackaday.com/2019/05/09/stator-library-makes-your-arduino-code-easier-to-read/>

代码的可读性决定了你的项目是一件令人愉快的工作，还是一件令人头疼的事情。这在与他人合作时会加倍。拥有容易解析的代码可以减少你的认知负荷，让解决问题变得更容易。为了帮助解决这个问题， [[PTS93]开发了定子库，使得一些常见的任务更容易阅读。](https://github.com/PTS93/Stator)

该库的目的是消除成堆的状态跟踪变量和无尽的 if/else 语句——因此得名。它主要是为 Arduino IDE 设计的，但对 API 没有任何依赖性，所以可以在其他 C++环境中使用。它附带了各种用于常见工作的简洁工具，例如读取触发点周围具有迟滞的模拟传感器，以及跟踪多个变量的状态变化的简单方法。通过使用基本的英语术语，而不是条件检查和数学运算符，它可以使事情更具可读性，更容易理解。

Arduino 平台的强大之处一直在于其易于使用的库，这些库使一切都变得更容易，从连接液晶显示器到使用亚马逊 Dash 按钮的[。](https://hackaday.com/2017/02/02/dash-with-arduino/)