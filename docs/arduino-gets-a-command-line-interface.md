# Arduino 得到一个命令行界面

> 原文：<https://hackaday.com/2018/11/10/arduino-gets-a-command-line-interface/>

当使用 Arduino 时，至少一旦你通过了闪烁的 led，你可以开始利用串行连接来发送和接收来自微控制器的信息。在主板与其环境交互时与主板通信是实时获取信息的重要方式。通常，这就是它所能做到的，但是[Pieter]想在 Arduino 的命令行解释器(CLI)上更进一步。

CLI 允许用户直接在 Arduino 上运行类似 Unix 的命令。这意味着通过命令行控制 GPIO 和微控制器的其他功能。CLI 在微控制器和您在计算机上选择的 ANSI/VT100 终端仿真器之间进行通信，支持大量与 Arduino 交互的新方法。

CLI 要求将一个十六进制文件加载到 Arduino 上，这个文件[可以在一个单独的站点](https://piconomix.com/fwlib/_a_r_d_u_i_n_o__u_n_o__b_o_a_r_d__a_p_p__c_l_i.html)找到，也是由【Pieter】维护的。一旦运行了，你就可以从你的 Arduino 中得到所有的命令行的好处。[Pieter]在他的项目页面上也有一些例子，以及完成设置和运行的完整方法。在命令行世界，在 Linux 和 [windows](https://hackaday.com/2016/03/30/windows-and-ubuntu-cygwin-can-suck-it/) 中有很多[正在进行。所以那里也有很多值得探索的地方。](https://hackaday.com/2018/10/24/linux-fu-marker-is-a-command-line-menu/)