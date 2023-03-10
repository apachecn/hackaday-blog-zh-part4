# 使用 2020 机器视觉拨入您的多头 3D 打印机

> 原文：<https://hackaday.com/2020/06/14/dial-in-your-multi-headed-3d-printer-with-2020-machine-vision/>

大多数一直在探索多工具 3D 打印的人都知道，排列喷嘴可能是一个棘手的问题，但却是必要的痛点。现有的方法要么让我们用游标卡尺测量偏移量，要么用朝上的相机拍摄一系列照片。而这一步是不容忽视的！喷嘴之间的任何不匹配，你的多色打印最终看起来像斯科蒂真的搞砸了传输梁控制台上的滑块。然而，不要害怕！[Danal]把这个问题作为一个机会来写一些完全自动化的东西，通过机器视觉带给你。

被称为 *TAMV* 的*工具对准机器视觉*，【Danal】除了一个朝上的摄像头之外，还在他现有的 3D 打印运动控制器旁边添加了一个树莓 Pi。几行代码(和几个小时的 OpenCV 编译)之后，他自己有了一个圆检测脚本，它自动循环通过每个工具，检测喷嘴中心，并计算每个工具的偏移，存储在机器的配置文件中。如果这还不够漂亮的话，他已经将整个设置开源了，他包括了一个用于编译 OpenCV 的安装脚本和一套精心编写的[逐步说明](https://jubilee3d.com/index.php?title=TAMV)。

在一个大多数业余爱好者仍然手动解决这个问题的世界里，这是超越我们所知的飞跃，是建立在可识别的硬件和软件之上的机器视觉的伟大应用。虽然该项目是为运行 Duet3 控制器的 [Jubilee](https://hackaday.com/2019/11/14/jubilee-a-toolchanging-homage-to-3d-printer-hackers-everywhere/) 配备的，该控制器带有以“单板计算机”模式连接的 Raspberry Pi，但其核心功能很容易适应任何其他具有类似控制板堆栈的多工具机床。对于愿意深入了解的人来说，该项目甚至可以扩展为一个独立的脚本，您可以在本地 PC 上运行该脚本来单独打印刀具补偿。

与 TAMV 一样，令人耳目一新的是，即使在 3D 打印机问世十年后，我们仍在寻找让这些机器功能更强大的方法。对于这一类别的更多新内容，请查看使用 [sharpie ink 作为支持材料脱模剂](https://hackaday.com/2020/05/27/improving-3d-printed-supports-with-a-marker/)的新方法。

令人难过的是，[Danal]最近在上周去世了，但我们很高兴能捕捉到这个人的生活历史的快照。

 [https://www.youtube.com/embed/e_d_XHwGfRM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e_d_XHwGfRM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

