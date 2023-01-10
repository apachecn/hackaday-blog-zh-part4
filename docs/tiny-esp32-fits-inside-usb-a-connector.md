# 微型 ESP32 适合 USB-A 连接器

> 原文：<https://hackaday.com/2019/09/28/tiny-esp32-fits-inside-usb-a-connector/>

几年前推出的 ESP32 是一种为各种微控制器配备 WiFi 或蓝牙的廉价方式。从那时起，由于它与 ESP8266 的相似性和易于编程的能力，它一直在进行实验和开发。随着这个小芯片的不断成长，观察它的发展确实令人着迷。[或者，在这种情况下，收缩](https://hackaday.io/project/167005-femu-an-esp32-wi-fibluetooth-board-in-tomu-form)。

ESP32 世界的最新发展来自[femtoduino]，顾名思义，它制造非常小的东西。这是一个完整的 ESP32，适合 USB-A 连接器。该项目的大脑是 ESP32-D2WD，这是一个具有 2 Mb 内存的双核芯片，使其功能更加强大。事实上，这个项目的很大一部分是[femtoduino]对 MicroPython 的修改，以便允许它在这个芯片组上运行。仅此一点，就很酷。

这个项目令人印象深刻，因为它的规模和对 MicroPython 库的添加。如果你需要一些非常非常小的东西，不管出于什么原因，你可能会想要选择其中的一个。不过要小心，并且[确保获得最新版本的 SDK](https://hackaday.com/2019/09/05/esp8266-and-esp32-wifi-hacked/) 。