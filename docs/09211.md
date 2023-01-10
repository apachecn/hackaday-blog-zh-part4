# 从旧笔记本电脑构建廉价的 Kubernetes 集群

> 原文：<https://hackaday.com/2021/02/08/building-a-cheap-kubernetes-cluster-from-old-laptops/>

集群计算是重型计算应用的流行选择。在基础级别，有通常用 Raspberry Pis 构建的爱好集群，而工业级别涉及挤满全速运行的服务器的数据中心。[greg]想要便宜的东西，但要有 x86 支持–[所以开始以自己的方式构建一个平台。](https://stencel.io/posts/build-cheapest-kubernetes-i7-cluster.html)

[greg]构建的巧妙部分来自源计算机。他发现替换的笔记本电脑主板是廉价的计算能力的重要来源，易贝的 i7 CPU 和 16GB 内存的主板售价约为 100 英镑，i5 型号甚至更便宜。手头有了四块笔记本电脑主板，他开始把它们叠放在一个箱子里，给它们通电，用最少的工作所需的东西把它们连接起来。所有东西都包装在一个旧的服务器机箱中，并用一些 3D 打印部件将它们固定在一起，他能够以绝对低廉的价格启动并运行一个 4 节点 Kubernetes 集群。

我们以前从未见过以这种方式使用备用笔记本电脑主板，但我们肯定会看到这种情况越来越多。对于那些廉价构建集群的人来说，装满废弃主板的板条箱的可能性很诱人。当然，节点越多越好，[所以看看这个 120 Pi 的集群，满足你对 *raw FLOPs 的渴望。*](https://hackaday.com/2014/10/07/120-node-rasperry-pi-cluster-for-website-testing/)