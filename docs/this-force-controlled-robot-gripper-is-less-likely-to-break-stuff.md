# 这种力控制的机器人手爪不太可能打碎东西

> 原文：<https://hackaday.com/2019/03/25/this-force-controlled-robot-gripper-is-less-likely-to-break-stuff/>

虽然机械臂可以处理各种各样的任务，但手头的具体工作将对所使用的末端执行器的类型产生重大影响。对于分类铁磁部件，电磁体可能就足够了，而为了更精确的定位，可以使用机械夹具。如果你正在处理特别精细的物体或者与人合作，可能需要一个力控制的手爪来避免损坏。为了这个目的，詹姆斯·布鲁顿(James Bruton)已经开始了他自己的设计。

基本的手爪是 3D 打印的，有 3 个手指，每个手指由两个关节组成。每个手指的收缩是由橡皮筋完成的，而伸展是通过一个连接在手指上的伺服机构通过弹簧完成的。每个手指的位置用一个电阻弯曲传感器来测量。Arduino Uno 用于运行伺服系统和读取连接的传感器。

当伺服系统施加力时，弹簧开始拉伸。随着施加的力增加，这导致伺服位置和手指位置之间的差异更大。通过计算这个差值，就可以确定手指施加的力。这可以用来限制手爪施加的力，以避免打碎易碎的物体或压碎柔软、多肉的人。

[James]注意到当前的设计有一些缺点。移动手指所需的力沿着它们的行程是不一致的，这在某种程度上干扰了精确的测量。总的来说，这是概念的可靠证明，也是进一步修改的良好基础。Github 上的文件是为那些希望在家修补的人准备的。

意识到在机械环境中施加的力是获得好结果的关键。我们甚至看到了为这一目的而改装的手扳压机。休息后的视频。

 [https://www.youtube.com/embed/V0Y4mJLtLFU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/V0Y4mJLtLFU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

