# 带中断和 IRAM 的 ESP32 音频采样

> 原文：<https://hackaday.com/2019/12/07/esp32-audio-sampling-with-interrupts-and-iram/>

打断别人的谈话对人类来说是粗鲁的，但对计算机来说是聪明的。[Ivan Voras]展示了在对声音进行采样时，如何使用中断[为 ESP32 模数转换器提供服务。有趣的是，他使用混合了原生 ESP-IDF API 的 Arduino IDE 来获得最佳性能。](https://www.toptal.com/embedded/esp32-audio-sampling)

像大多数复杂的中断驱动软件一样，[Ivan 的]代码使用两阶段中断策略。当定时器到期时，中断发生。处理程序需要快速完成，所以它除了设置一个标志之外什么也不做。另一个例程在标志上阻塞，然后执行所需的实际工作。

因为中断服务程序需要很快，所以它必须在 RAM 中。[Ivan]使用 IRAM_ATTR 属性来实现这一点，并解释当您使用它时会发生什么。

> CPU 内核只能从嵌入式 RAM 中执行指令(并访问数据)，而不能从通常存储程序代码和数据的闪存中执行指令。为了解决这个问题，总容量为 520 KiB 的 RAM 中有一部分专用于 IRAM，这是一个 128 KiB 的缓存，用于透明地从闪存中加载代码。ESP32 对代码和数据使用单独的总线(“哈佛架构”)，因此它们被分开处理，这扩展到了内存属性:IRAM 是特殊的，只能在 32 位地址边界访问。

这一点非常重要，因为一些 ESP-IDF 调用(包括 adc1_get_raw)不使用该属性，因此如果将它们推到闪存中，就会崩溃。最后，他在使用 ESP32 操作系统和裸机的好处之间沉思。

如果你想了解更多关于 ESP32 上的 [Arduino，我们已经报道过了。我们还](https://hackaday.com/2016/10/31/whats-new-esp-32-testing-the-arduino-esp32-library/)[深入研究了几次芯片](https://hackaday.com/2016/10/04/how-to-get-started-with-the-esp32/)。