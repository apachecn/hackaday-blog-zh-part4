# 很多 Blinky！ESP32 驱动 20，000 个 WS2812 LEDs

> 原文：<https://hackaday.com/2019/05/07/lots-of-blinky-esp32-drives-20000-ws2812-leds/>

20，000 个 led 听起来像是惊人的眨眼次数。当我们开始考虑将 20，000 个任何东西放在一起，然后用一小片邮票大小的电子设备来控制它们的过程时，我们有点头晕。

公平地说，我们不确定[yves-bazin]已经组装了 20，000 个 LED，但他已经证明了一次性驱动 20，000 个 led 的可行性，这要归功于 FastLED I2S 库的一些编辑和硬件 GPIO 扩展。诀窍在于使用移位寄存器将单个 ESP32 引脚转换为五个输出。使用 16 个 GPIO 引脚，每个引脚连接到 HC595 移位寄存器，所有引脚连接到相同的第 17 和第 18 个 GPIO 引脚用于锁存和时钟，这 16 个输出扩展到 80 个输出，用于驱动 256 个 WS2812s 的条带，产生 20480 个受控 led。移位寄存器方法允许 ESP32 以五倍于 LED 灯条的速度运行，因此它可以推出五个灯条的每个引脚上的位，锁存，然后对 256 个 LED 的每个位重复，然后重新开始下一帧。

[yves-bazin]尚未建立完整的 20，000 像素显示器，尽管他的视频确实展示了一个 6，000 像素的视频墙，但他能够通过将一个更小的面板连续插入每个输出来证明他的概念正在工作，以显示正确的信号仍然以令人印象深刻的 130 fps 从所有 80 个条带的 ESP32 中发出。

[演示视频在 reddit](https://old.reddit.com/r/esp32/comments/bkyeq0/20000_ws2812b_pushed_at_130fps_with_esp32_and/) 上。使用 [74HC595 移位寄存器进行 GPIO 扩展](https://hackaday.com/2018/06/14/general-purpose-i-o-how-to-get-more/)并不是什么新鲜事，我们已经见过一个 [ESP8266，它带有用于 157 个灯的移位寄存器](https://hackaday.com/2018/03/16/massive-shift-register-switches-lights/)，但使用它来控制 20k LEDs 令人印象深刻，尤其是现在有了一个用于 ESP32 的库。带上你的太阳镜。