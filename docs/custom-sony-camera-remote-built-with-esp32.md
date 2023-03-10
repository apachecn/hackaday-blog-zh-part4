# 定制索尼相机遥控器，内置 ESP32

> 原文：<https://hackaday.com/2022/10/21/custom-sony-camera-remote-built-with-esp32/>

无论你是拍摄视频还是照片，拥有一个相机遥控器真的可以提高你的工作效率。你再也不用跑回到相机前按下它的小按钮了！[Frank Zhao]是一名索尼用户，因此决定使用 ESP32 为他的 Alpha 相机定制一个遥控器，[同时添加一些特殊功能。](https://eleccelerator.com/alpha-fairy-wireless-camera-remote/)

[![](img/887154756d4860c0aac084dbb1bd480b.png)](https://hackaday.com/wp-content/uploads/2022/10/sonyremote_detail.jpg) 该构建通过 WiFi 与相机通信，但如果无线电链路出现问题，可以退回到红外线。它是围绕 M5StickC 构建的，M5 stickc 是一种预构建的设备，具有 ESP32 和手持式小显示器。这让他可以将遥控器的尺寸缩小到索尼官方设备的一半。虽然板上的按钮有限，但他依靠 IMU 来控制许多运动手势的高级功能。

遥控器可以实现索尼在出厂时没有内置到相机中的一系列功能。有一个声音激活的快门释放，双快门模式，和几个基于定时器的工具，包括天文摄影模式。还有一个很大的旋钮，你可以添加焦距，还有一个模式，当你对它不能正常工作感到沮丧时，可以重置自动对焦。有些功能比其他功能更好，因为有时相机对命令的响应不够快。无论如何，[弗兰克]用他定制的 20 美元的遥控器释放了如此多的额外功能，这是非常棒的。

我们以前也看到过其他自制工具为相机开辟新的创作可能性。如果你有自己漂亮的摄影技巧，[请告诉我们吧！](https://hackaday.com/submit-a-tip/)