# 一年后的系列工作室

> 原文：<https://hackaday.com/2022/01/15/serial-studio-one-year-on/>

去年我们[报道了【Alex Spataru】的串行工作室项目](https://hackaday.com/2021/01/31/serial-studio-easily-visualise-and-log-serial-data/)，该项目以串行端口数据可视化工具开始，就像一个增强版的 Arduino 串行绘图仪。[Alex]从那以后一直在积极改进该项目，添加了各种新功能，包括

*   数据格式的 JSON 编辑器
*   TCP、UDP 和多播
*   更加灵活的新型显示部件
*   多信号图
*   FFT 和对数图
*   VT-100 仿真
*   支持插件和主题
*   添加了 MQTT 支持

[Alex]最初提出 [Serial Studio](https://serial-studio.github.io/) 是因为他参与了各种 CanSat 项目的地面站软件，每个项目都有相似但略有不同的数据格式和显示要求。他没有制作几个不同的程序，而是决定制作可以使用 JSON 描述符文件进行配置的 Serial Studio。

该程序是开源的和多平台的。您可以自己构建它，或者下载预编译的 Windows、Linux 和 Mac 二进制文件。更多细节参见[项目 GitHub 资源库](https://github.com/Serial-Studio/Serial-Studio)。除了英语，它还被翻译成西班牙语、汉语和德语。如今，您最常用的串行数据遥测可视化工具是什么？请在下面的评论中告诉我们。