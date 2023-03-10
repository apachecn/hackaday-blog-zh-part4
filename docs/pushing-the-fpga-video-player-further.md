# 推动 FPGA 视频播放器进一步发展

> 原文：<https://hackaday.com/2020/11/30/pushing-the-fpga-video-player-further/>

黑客社区中众所周知的一个事实是，项目从来没有真正完成过。你总是可以再发布一个主板来修复一个丝网印刷的错误，获得额外的一点点性能提升，或者最终花时间跟踪那个奇怪的短暂错误。或者在[ultra embedded]的情况下，[从 800 x 600 到 1280 x 720](https://github.com/ultraembedded/FPGAmp) 取一个定制的 FPGA 播放器。使用的硬件是用于 I2S2、VGA 和 MicroSD 的 Digilent Arty A7 和 PMOD 板。我们之前在项目刚开始的时候[报道过这个项目。](https://hackaday.com/2020/09/26/an-fpga-video-player-built-just-for-fun/)

从 800 x 600 到 1280 x 720(增加 31%的像素)需要实施更高性能的 JPEG 解码器，该解码器可以读入 MPJEG 帧，每 2.1 个时钟周期推出一个像素。改进还包括一些方便的功能，如红外遥控器。系统中子模块的数量令人难以置信，其中大多数都是由[ultraembedded]自己实现或调整的。

对于 FPGA Verilog，有 SD/MMC 接口、JPEG 解码器、音频控制器、DVI 帧缓冲器、外设内核和定制 RISC-V CPU。对于从 SD 卡下载的固件，它使用自定义的 RTOS 运行 MP3 解码器、FAT32 接口、IR 解码器和基于 LVGL 的 UI。

我们认为这个项目代表了[ultraembedded]多年来生产的所有不同 IP 内核的完美顶峰。FPGA 媒体播放器的所有代码都可以在 GitHub 上获得。

> 我想我已经用#FPGA、#RISCV、#MJPEG 和 27，000 行 Verilog 为自己构建了一个高清(720p50)视频播放器！从 800×600 - >到 1280×720，又多了 10 MHz！实际上，我打算在这天晚上坐下来看一部电影！[https://t.co/4G1ZiN2ipY](https://t.co/TTG7huzyZW)
> 
> –ultra embedded(@ ultra embedded)[2020 年 11 月 21 日](https://twitter.com/ultraembedded/status/1330110294140596225)