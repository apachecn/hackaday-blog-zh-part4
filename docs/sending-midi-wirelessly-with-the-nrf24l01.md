# 使用 NRF24L01 无线发送 MIDI

> 原文：<https://hackaday.com/2022/02/17/sending-midi-wirelessly-with-the-nrf24l01/>

MIDI 是全世界音乐家和乐器都知道的标准。常规系列的基本变化帮助世界各地的工作室更有效地工作。[Kevin]想尝试无线发送 MIDI 数据，但与典型的蓝牙解决方案不同，[决定使用不起眼的 nRF24L01。](https://diyelectromusic.wordpress.com/2022/01/28/arduino-rf24-midi-interface/)

使用的电路很简单:[Kevin]简单地用 nRF24L01 无线电模块连接了两个 Arduino Unos，它们通过 SPI 进行通信。或者，更快的解决方案是使用 Keywish Arduino RF Nano，它在板上封装了 nRF24L01。一个 Arduino 可以连接到乐器的 MIDI 输出端口，它将无线发送 MIDI 信号。然后，第二个 Arduino 可以插入 MIDI IN 端口，并重复它通过无线接收的内容。

真正的工作是在固件中，它获取 MIDI 数据，并将其打包成合适的形式，通过 nRF24L01 发送出去。该系统可以在一对一模式下运行，模拟单条 MIDI 电缆，或[多播模式](https://diyelectromusic.wordpress.com/2022/02/14/arduino-rf24-midi-interface-part-2/)，其中一个发送者向许多接收者传输信息。

这是一个简洁的技巧，我们可以想象它在一些有趣的表演场合会很有用。我们也看到其他人为 Eurorack 硬件开发无线 MIDI 接口[。](https://hackaday.com/2019/02/21/eurorack-gets-a-wireless-midi-connection/)休息后的视频。

 [https://www.youtube.com/embed/Hj6LngiWFDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Hj6LngiWFDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

