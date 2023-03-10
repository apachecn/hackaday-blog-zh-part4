# 使用球形挠性接头的 3D 印刷操纵杆

> 原文：<https://hackaday.com/2021/05/25/3d-printed-joystick-using-spherical-flexure-joint/>

3D 打印带来的众多进步之一是柔顺机构和弯曲关节的快速发展。一个这样的例子是【jicerr】的[操纵杆](https://www.youtube.com/watch?v=n7yjRrHE-SI)，它使用了一对[球形弯曲关节](https://www.youtube.com/watch?v=DAngcygU7tc)，这是最近由荷兰代尔夫特理工大学的[研究人员开发的，请看休息后的视频。](https://www.sciencedirect.com/science/article/pii/S0141635921000726?via%3Dihub#appsec1)

两种弯曲关节设计都利用四面体形状的元件，允许物体像球窝关节一样围绕空间中的固定点枢转。其中一个关节名为 Tetra 2，非常适合在标准的 FDM 打印机上打印，3D 文件是由研究人员之一的[Jelle_Rommers]上传到 Thingiverse 的。[jicerr]采用了这一设计，并创建了一个底座，用于在距离焦点不远的地方安装 HMC5883 三轴磁力计，该磁力计可感应焦点处小磁铁的旋转。Arduino 接收磁力计的输出，进行必要的计算，并作为操纵杆与 PC 接口。通过在 Solidworks 中使用它来旋转和平移设计来演示这一点。这种设计需要记住的一点是，它需要一个固定的底座来防止它四处移动。还应该可以将设计直接集成到控制器的外壳中。

另一个有趣的应用是把它变成一个前面有鸡头的[笔筒，如【50Pro】所示。如果你对其他应用有任何想法，请在评论中提出。](https://www.youtube.com/watch?v=taodni2Mc7Q)

柔顺机构有许多有趣的应用，包括[谐波传动](https://hackaday.com/2021/04/07/harmonic-drive-uses-compliant-mechanism-to-slim-down/)、[千分表](https://hackaday.com/2020/07/15/no-assembly-required-for-this-compliant-mechanism-dial-indicator/)和[推力矢量支架](https://hackaday.com/2019/06/16/thrust-vectoring-with-compliant-mechanisms-is-hard/)。

 [https://www.youtube.com/embed/DAngcygU7tc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DAngcygU7tc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/n7yjRrHE-SI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/n7yjRrHE-SI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/taodni2Mc7Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/taodni2Mc7Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢提示[基思奥尔森]！