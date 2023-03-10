# 手动 3D 数字化仪有点像三维卷尺

> 原文：<https://hackaday.com/2018/12/21/manual-3d-digitizer-works-a-bit-like-3-dimensional-measuring-tape/>

将一个物体数字化通常意味着启动一个 CAD 程序，将卡尺放在手边，或者使用 3D 扫描仪创建一个代表物体表面的点云。[Dzl]用他的 [DIY 手动 3D 数字化仪](http://blog.dzl.dk/2018/08/21/3d-digitizer/)采取了一种完全不同的方法，这是一种激光切割和 3D 打印的组件，使用旋转编码器创建一个附有铰接“探针臂”的转盘。

手臂的每个关节也是一个编码器，通过读取编码器值并应用一点三角学，可以随时知道手臂尖端的相对位置。因此，在物体上从一个点到另一个点手动移动臂的尖端会产生该物体的测量值。[Dzl]成功地创建了一个原型来测试这个想法，项目文件在 GitHub 上有[可用。](https://github.com/dzlonline/3D_digitizer2)

我们还记得这个项目的[早期版本，很高兴看到它是如何更新的，比如增加了一个带编码器的转盘。DIY 3D 数字化采用了各种方法，其中一个例子是](https://hackaday.com/2015/05/19/an-open-source-diy-digitizer/)[这个单元使用了四个 Raspberry Pi 零和四个摄像头](https://hackaday.com/2018/01/17/four-pi-zeros-four-cameras-one-really-neat-3d-scanner/)来生成高质量的 3D 扫描。