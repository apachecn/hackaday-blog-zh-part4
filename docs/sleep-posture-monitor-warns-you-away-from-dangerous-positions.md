# 睡眠姿势监视器警告你远离危险的姿势

> 原文：<https://hackaday.com/2022/08/28/sleep-posture-monitor-warns-you-away-from-dangerous-positions/>

我们被告知，年龄只是一个数字，但这个数字似乎是不断增加的荒谬性质的伤害计数。曾经年轻版的我们可以从行驶中的汽车上跳下来，或者从树上掉下来，只有几处擦伤以示努力，增加几十次围绕太阳的旅行，你会发现仅仅“睡觉滑稽”就可以让你一周不能工作。

为了避免这种不幸，[精英虫]想出了这种睡眠姿势警报来监视夜间的侵犯行为，因为他注意到转换到脸朝下的睡眠姿势会使他的脖子扭结。他首先考虑使用简单的机械倾斜开关来检测从仰卧到俯卧的无意识偏移。但是为了不被固定在一个姿势上，他决定用加速度计来代替。IMU 和 ATtiny85 与一个小型振动电机一起位于一个定制的 PCB 上，与蜂鸣器或传呼机相比，它允许更多的离散警报。

放置在 3D 打印的外壳中，夹在他的短裤上，这款可穿戴设备就可以使用了。微控制器每八秒钟醒来一次，检查自己的位置，如果他进入痛苦的区域，就会发出警报。[Elite]对该设备进行了一些功率分析，虽然还有改进的空间，但目前估计的 18 天充电间隔并不算太差。下面的视频有所有的细节；希望设计文件和代码很快会出现在他的 GitHub 上。

考虑到我们大多数人一生中有三分之一的时间在睡觉，难怪黑客们兴致勃勃地解决睡眠问题。从[观察你的脑波](https://hackaday.com/2022/06/15/a-sleep-monitor-for-minimum-outlay/)到[人工智能生成的胡言乱语 ASMR](https://hackaday.com/2022/03/26/ai-generated-sleep-podcast-urges-you-to-imagine-pleasant-nonsense/) ，一旦你的头碰到枕头，就会有大量的黑客素材。

 [https://www.youtube.com/embed/ab_7tqleNow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ab_7tqleNow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

