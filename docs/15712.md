# 针对最大闪烁量优化的 LED 圣诞灯

> 原文：<https://hackaday.com/2022/12/21/led-christmas-lights-optimized-for-max-twinkleage/>

老派的灯丝圣诞灯过去常常以闪烁的形式出现。发光二极管有着开关难的特性，不容易产生这种行为。为了纠正这一点，不久前， [[Mark Kriegsman]开发了一个 Arduino 程序，让 led 闪烁得非常漂亮。](https://gist.github.com/kriegsman/756ea6dcae8e30845b5a)

该计划被称为 TwinkleFOX，并依赖于流行的 [FastLED 库](https://hackaday.com/2015/05/10/roswell-eat-your-heart-out/)用于可寻址 LED。[Mark 的]演示设置是围绕使用 WS2811 LEDs 构建的，这些 led 通过每个灯泡上的塑料扩散器串联在一起。Arduino 被编程为根据三角波函数改变每个 LED 的亮度。为了创造闪烁的效果，每个 LED 都有自己独特的时钟信号，因此它们在不同的时间以不同的速率改变亮度。

使用 Arduino Uno 或 Leonardo，[Mark]报告说它可以以每秒超过 50 次更新的速度闪烁 300 个独立的 led。使用一个更快的微控制器应该可以在更长的字符串中获得可靠的性能。同时，如果你想知道老式灯过去是如何闪烁的，[我们以前也讨论过这个问题](https://hackaday.com/2018/01/07/the-secret-of-twinkling-christmas-lights/#:~:text=Typical%20flashing%20bulbs%20use%20a,lights%20do%20exactly%20the%20opposite.)。休息后的视频。

 [https://www.youtube.com/embed/CqCaF1bD4Uk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CqCaF1bD4Uk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

