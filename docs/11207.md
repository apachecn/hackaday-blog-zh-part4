# 智能激光切割机 Ad-on 光学检测材料

> 原文：<https://hackaday.com/2021/09/06/smart-laser-cutter-ad-on-detects-material-optically/>

拜托，承认吧。你已经做到了。我们做到了。你知道——你真的确定你在黑客空间发现的那张塑料纸是丙烯酸的，对吗？你拨入设置，加载设计，设置焦点，按下绿色的“开始”按钮。当你冲向红色的“停止”按钮时，大量的黑烟、火焰和普遍的不良后果随之而来，然后揭开盖子，想出如何清理这个。

那不是丙烯酸。那是聚碳酸酯。

你需要的是麻省理工学院的最新小工具: [SensiCut:一个智能激光切割机系统，可以自动检测不同的材料](https://news.mit.edu/2021/smart-laser-cutter-system-detects-different-materials-0819)。

这项技术利用了所谓的“散斑成像”,即激光照射的材料会在相机中产生独特的反射斑点或散斑图案。通过用大量样本训练深度神经模型，发现可以以 98%的准确度检测多达 30 种类型的材料。

预烤模型运行在一个树莓 PI zero 上，带有现成的摄像头，全部由一个电源组供电。这允许整个组件简单地落在现有的激光切割头上，不需要布线。

即使你是一个经验丰富的激光切割机用户，拥有一个控制良好的库存堆，这可以让你放心，这绝对值得努力。更详细的描述和更多视频可以通过[阅读全文](https://hcie.csail.mit.edu/research/sensicut/sensicut.html)找到。我们希望在不远的将来，他们会把这个系统作为开源软件发布。如果没有，那么，你知道该怎么做:)

 [https://www.youtube.com/embed/1CjrVntolmo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1CjrVntolmo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

