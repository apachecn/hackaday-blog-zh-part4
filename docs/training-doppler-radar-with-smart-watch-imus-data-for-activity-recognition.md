# 利用智能手表 IMUs 数据训练多普勒雷达进行活动识别

> 原文：<https://hackaday.com/2022/04/30/training-doppler-radar-with-smart-watch-imus-data-for-activity-recognition/>

当涉及到自动解释传感器数据时，拥有一个大型数据集来帮助验证它，以及在涉及机器学习(ML)时进行训练，这是有帮助的。用仔细标记和分类的信息创建这个数据集是一个漫长而乏味的过程，这就是跨域翻译的想法发挥作用的地方，例如在卡内基梅隆大学 Smash 实验室的 [IMU2Doppler 项目中使用毫米波(mmWave)雷达传感器来识别建筑物居住者的活动。](http://smashlab.io/publications/imu2dop/)

在对人体运动进行分类时，最常用的传感器类型是惯性测量单元( [IMU](https://en.wikipedia.org/wiki/Inertial_measurement_unit) )，如加速度计和陀螺仪，从智能手机到智能手表和健身带，这些传感器随处可见。对于这些设备，通常将测量模式分类为匹配特定活动，如散步、慢跑或刷牙。这使得它们定义明确，非常容易理解。

至于为什么基于毫米波的多普勒雷达更适合用于监控建筑物内的人员，与使用摄像机相比，这是隐私方面的问题，而且给人们配备一个体戴式 IMU 也不方便。使用多普勒雷达，理论上人们可以跟踪自己家中的活动，也可以在医疗环境中确保病人的安全，或者在健身房跟踪一个人的表现或设备的使用。所有这些都不需要使用相机或个人传感器。在过去，我们已经看到了一个[类似的方法，使用目标激光束](https://hackaday.com/2018/10/22/vibrosight-hears-when-you-are-sleeping-it-knows-when-youre-awake/)。

虽然听起来很有希望，但在这个时间点上，以合理的准确度(约 70%)被识别的活动的数量仅限于十种类型。根据预期的应用，这可能已经足够了，尽管正如[发表的论文](http://smashlab.io/pdfs/imu2dop.pdf)指出的，仍然有很大的增长空间。

 [https://www.youtube.com/embed/3EbK2MT-fDk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3EbK2MT-fDk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

