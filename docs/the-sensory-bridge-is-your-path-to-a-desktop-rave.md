# 感官桥是你通向桌面狂欢的道路

> 原文：<https://hackaday.com/2022/09/26/the-sensory-bridge-is-your-path-to-a-desktop-rave/>

[谢利实验室]对于用 led 或其他显示器创建许多项目并不陌生。现在他们创造了一种低延迟的音乐可视化工具，叫做[感官桥](https://sensorybridge.rocks/)，可以从音乐中创造出华丽的灯光表演。

Sensory Bridge 能够以 60 fps 的速度更新多达 128 个 RGB LEDs。该装置有一个板载 MEMS 麦克风，可以拾取环境音乐以产生灯光表演。该芯片是一个 ESP32-S2，进行快速傅立叶变换欺骗，允许实时更新 RGB 阵列。LED 端子支持常见的 WS2812B LED 引脚排列(5 V，GND，数据)。Sensory Bridge 还有一个“附件端口”，可用于硬件扩展，例如他们的 LED“迷你桅杆”的底座，这是一个长的 RGB 阵列 PCB 带。

该装置由一个 5 V 2 A USB-C 连接器供电。设备上的不同旋钮调节 LED 灯条的亮度、麦克风灵敏度和反应性。其中一个更好的功能是它的“噪音校准”，可以记录环境声音，并减去背景噪音频率成分，以提供更清晰的音乐信号。Sensory Bridge 仍然是新的，看起来有些功能还没有到来，如 WiFi 通信、附件端口升级和 3.5 毫米音频输入，以绕过板载麦克风。

感官桥的既定目标是提供一个开放、强大和灵活的平台。这可以从他们承诺[将项目](https://github.com/connornishijima/SensoryBridge)作为开源硬件发布，提供固件、PCB 设计文件，甚至是 libre/free 许可下的 case STLs 中看出来。音频频谱分析仪是我们的最爱，我们已经看到了许多不同的迭代，从使用 [Raspberry Pis](https://hackaday.com/2021/02/22/led-spectrum-visualizer-driven-by-raspberry-pi/) 到其他使用 [ESP32s](https://hackaday.com/2020/12/10/esp32-spectrum-analyzer-taps-into-both-cores/) 的。

休息后的视频！

 [https://www.youtube.com/embed/4ALef1g3c2c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4ALef1g3c2c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

