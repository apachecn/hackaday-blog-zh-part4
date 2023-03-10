# 行动相机的外部电池模块可以无损地做到这一点

> 原文：<https://hackaday.com/2020/06/09/external-battery-mod-for-action-camera-does-it-non-destructively/>

[![](img/e791aae3a62c9de2936d4263b6ece8b6.png)](https://hackaday.com/wp-content/uploads/2020/06/img_20200510_134545.jpg) 【无脸科技】拥有一台 SJCAM SJ4000 动作相机，但内部电池不再工作。不希望购买替代品，也不愿意连接笨拙的 USB 电缆来供电，解决方案是[设计和 3D 打印一个适配器，用一个可充电的 14500 大小的电池](https://facelesstech.wordpress.com/2020/05/10/sj4000-action-cam-14500-battery-mod/)(它与 AA 电池大小相同，与相机的宽度很匹配。)

[![](img/588f999b7ee2e8a690cbaa664976af5c.png)](https://hackaday.com/wp-content/uploads/2020/06/Female-header-closeup.jpg) 适配器是通过模仿原厂电池来工作的，所以相机永远不会知道其中的区别。14500 电池的 3D 打印支架(兼作 GoPro 兼容支架)具有与相机原始内部电池相同大小和形状的延伸部分。棘手的部分是连接埋在相机电池仓内的电源连接器。为了解决这个问题，[Facelesstech]最终选定了从一个母接头内部获取的小连接器，用它们来连接相机内部的小刀片。我们打破了一个备用的女性 0.1 英寸的标题，显示在这里，以明确这些小零件从何而来。唯一需要的其他电池硬件是 AA 电池的触点，但这些也很容易收获和重复使用。

项目的 [GitHub 库包括 STL 文件以及零件的 FreeCAD 文件。下面嵌入了视频概述。](https://github.com/facelessloser/SJ4000_14500_battery_mod)

 [https://www.youtube.com/embed/U0X0NFQgeq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U0X0NFQgeq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[也可以为这些相机添加外部麦克风输入](https://hackaday.com/2017/05/31/hacking-an-external-mic-port-onto-a-camera/)，但这比外部电源要复杂得多。