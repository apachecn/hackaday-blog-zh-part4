# 学习树莓 Pi Mandelbrot 集群的诀窍

> 原文：<https://hackaday.com/2022/01/18/learning-the-ropes-with-a-raspberry-pi-mandelbrot-cluster/>

你可能听说过这样的说法:将一堆树莓聚在一起组成一台“超级计算机”没有多大意义，因为即使是一台普通的台式机也可能在性能方面超过它。虽然这可能是真的，但大多数人制造 Pi 集群的原因并不是为了原始能力，而是为了在不倾家荡产的情况下积累并行计算的经验。

因此，尽管可能有一种“更好”的方式来制作下面的 Mandelbrot 视频，但创作者 [[Michael Kohn]仍然学到了很多关于使用 Kubernetes 和 Docker 等行业标准工具来构建一个健壮的并行处理环境](https://www.mikekohn.net/software/mandelbrots_cluster.php)的知识。对我们来说幸运的是，他好心地记录了整个过程，供其他可能有兴趣追随他脚步的人参考。无论您的并行任务是什么，也无论它运行在什么平台上，这里的一些注释都有可能帮助您完成它。

这不是我们见过的最大的树莓 Pi 集群，但是四个 Pi 4s 和它们所在的 RGB LED 花彩围栏构成了一个负担得起且节省空间的集群，可以磨练你的技能。无论您是在为软件开发和部署的未来而实践，还是只是在寻找新的东西来玩，[构建这些小规模集群之一](https://hackaday.com/2020/04/24/raspberry-pi-cluster-shows-you-the-ropes/)都是参与其中的好方法。

 [https://www.youtube.com/embed/qPHeCIEUwjw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qPHeCIEUwjw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

