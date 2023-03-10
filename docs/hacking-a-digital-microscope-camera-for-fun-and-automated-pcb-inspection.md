# 破解数码显微镜摄像头，实现有趣的自动化 PCB 检测

> 原文：<https://hackaday.com/2021/03/17/hacking-a-digital-microscope-camera-for-fun-and-automated-pcb-inspection/>

对自动化 PCB 检测的渴望让[charliex]陷入了一些深不可测的陷阱。他编写了自己的检测软件，他把 PCB 老虎钳安装在步进控制的工作台上，现在他[黑进了他的数码显微镜摄像头，允许远程和自动控制](https://charliex2.wordpress.com/2020/01/14/eakins-camera-hackery-pokery-and-the-legend-of-measuretwice/)。

对于电子爱好者来说，Eakins 相机已经成为一种相对流行、相对便宜的选择，用于检查他们的小规模工作。相机有一个用于鼠标的 USB 端口，并在 HDMI 输出上覆盖一个 GUI，用于控制相机的各种设置和将图像捕捉到 SD 卡。然而，使用基于鼠标的 GUI 会感觉笨拙，所以[用户已经努力简化流程](https://hackaday.com/2018/11/12/arduino-provides-hands-free-focus-for-digital-inspection-scope/)以更好地适应他们的工作流程。[charliex]决定进一步简化流程。

![](img/c862b5ea6301cfa6a68b29af6b871332.png)

显微镜摄影的一个问题是显微镜的焦平面非常紧。因此，即使在 SMD 电路板的微小尺度上，元件也太高了。一次只能聚焦一个亚毫米厚的层。如果你只拍一张照片，你想看的很多东西都会消失在模糊的距离中。焦点叠加通过在不同深度拍摄多张照片，然后将它们的聚焦位组合成一张清晰的图像来解决这个问题。

这解决了焦点问题，但是考虑到需要大量的图片，即使是最精简和直观的手动控制也会变得乏味。所以[charliex]寻找一种方法来远程控制他的相机，自动对焦堆叠，甚至可能进行全 PCB 扫描。

他首先打开检查工具，检查其内部结构。在里面，他找到了一个串行接口的焊点，并用他喜欢的废弃三星 USB 电缆将其连接起来。串行连接发出了一连串的启动消息，并立即给他一个进入 Hi3516A IP Camera Linux SoC 的根 shell，因此他开始四处探索，看看在引擎盖下事情是如何运行的。使用 *strace* 查看 GUI 进程(其描述性名称为 *myTest* )，他发现它使用本地套接字与单独的程序 *3516a_proc* 进行通信，该程序实际上通过 i2c 控制相机硬件。在捕获了 GUI 的每个相机控件(对焦、白平衡、图像捕获等)的信号后，只需构建、编译和上传他自己的可执行文件，就可以随心所欲地重放这些信号了。

![](img/eb3b532808d68ab7bb993038a20caefe.png)

Before and after focus stacking.

该项目的 GitHub repo 已经更新了一个支持 USB 以太网适配器的内核模块，使[charliex]能够通过网络控制他的相机。但是，最初仍然需要串行连接，以便在摄像机上加载和运行这些定制。他还改进了他的虎钳台，[引入了另一个维度的运动](https://charliex2.wordpress.com/2020/06/07/stick-vise-xy-table/)，并有一个老鹰示意叠加工作。这是一个非常有趣的正在进行的项目，我们期待更多的更新。如果这还不足以满足你的 PCB 检测需求，[你可能不得不超越可见光谱](https://hackaday.com/2018/10/12/seeing-a-webcams-pcbs-in-a-whole-different-light/)。

查看下面的快速视频，了解自动对焦堆叠捕捉的实际操作。

 [https://www.youtube.com/embed/tRmd8nV61Ds?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tRmd8nV61Ds?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

