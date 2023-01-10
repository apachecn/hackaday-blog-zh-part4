# 机器视觉跟踪肮脏的手

> 原文：<https://hackaday.com/2020/04/07/machine-vision-keeps-track-of-grubby-hands/>

你能记得你在某一天接触过的所有东西吗？如果你是诚实的，答案是，“可能不会。”我们人类是一个触觉物种，我们的运动和感觉神经有很大一部分直接传到我们的手上。我们通过手与世界互动，不幸的是，这可能意味着无意中传播疾病。

[Nick Bild]有一个潜在的解决方案:[一个名为 Deep Clean](https://github.com/nickbild/deepclean) 的机器视觉系统，它监控一个场景并记录其中任何被触摸的东西。[Nick]的系统使用 Jetson Xavier 和立体摄像机来检测场景中的深度；他用一对 Raspberry Pi 摄像头和一个 Pi 3B+构建了他的相机，但 Kinect 等其他深度相机可能也能完成这项工作。这个想法是观察人手的场景——open pose 是他为这项工作选择的工具——并将他们在场景中的深度与对象的深度相关联。触摸门把手或电灯开关，现场会留下一个标记。这个想法是，清洁人员将能够查看现场，以确定哪些区域需要额外的关注。我们可以想到许多超越当前危机的应用，因为绘制被触及区域的地图的能力似乎普遍有用。

[Nick]最近已经从 Xavier 那里获得了一些收益——他用它建造了[人工智能裁判](https://hackaday.com/2019/12/10/ai-knows-if-the-pitch-is-on-target-before-you-do/)和[灯罩，帮助你找到丢失的东西](https://hackaday.com/2019/12/07/upgrade-your-shades-to-find-lost-items/)。谁知道在监禁的这段时间里，他还会用它们做些什么呢？

 [https://www.youtube.com/embed/Qy8Ks7UTtrA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Qy8Ks7UTtrA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

