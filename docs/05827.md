# 阿多拉-BLE 合成墙没有电线

> 原文：<https://hackaday.com/2020/02/29/adora-ble-synth-wails-without-wires/>

这难道不是你见过的最可爱的小合成器吗？从视觉上来说，匹配的闪闪发光的半堆叠放大器真的很好。但是最有趣的部分呢？看不见一根电线，因为[【Blitz City DIY】的未来派钻机通过蓝牙 LE](https://www.thingiverse.com/thing:4144262) 发送哔哔声。

硬件方面，合成器和放大器都相当简单。在每一个可爱的小印刷按键下面都有一个通常带有原色明亮按钮帽的 clicky momentaries 按键本身只是压在顶部。所有 12 个电子琴和象牙琴都连接到 Adafruit 羽毛上，通过蓝牙 LE 与放大器中的 CircuitPlayground Bluefruit (CPB)进行通信。每次在 synth 上播放一个音符，其对应的颜色就会像彗星一样围绕着 CPB 的新像素，这些新像素通过放大器的扬声器格栅发光。

超级有趣的部分是，所有的艰苦工作都发生在代码中。两块板都有相同的彩虹顺序的颜色阵列，CPB 有一系列与颜色一一匹配的音调频率。对于弹奏的每个音符，CPB 会查找颜色，旋转颜色，然后弹奏音符。如果你想建造一个，这个项目是完全开放的——[ Blitz City DIY]甚至制作了一个学习指南，里面有所有肮脏的细节。休息后，请务必查看演示和扩展演练。

更多地在市场上制造电脑键盘？[拿最近的 ESP32](https://hackaday.com/2020/02/13/emulating-a-bluetooth-keyboard-with-the-esp32) 就行了。

 [https://www.youtube.com/embed/mBScFbHKeEY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mBScFbHKeEY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通路〔t0〕adafruit〔t1〕