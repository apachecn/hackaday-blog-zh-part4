# 从公共领域图像生成甲虫

> 原文：<https://hackaday.com/2020/01/12/generating-beetles-from-public-domain-images/>

自从[Ian Goodfellow]和他的同事在 2014 年发明了生成对抗网络(GAN)以来，数百个项目，从风格转换到诗歌生成器，都是使用竞争神经网络的概念产生的。与传统的神经网络不同，GANs 可以生成新的数据，这些数据在统计上符合与训练集相同的集。

[cunicode]背后的一个人设计团队[伯纳特·库尼]想出了用这种技术生成甲虫的主意。受到发表在[艺术家机器学习](https://ml4a.github.io/)上的材料的启发，他决定部署一些带有动物学插图的视觉实验。训练数据是从 archive.org 托管的公共领域书籍中找到的，该书籍是通过生物多样性遗产图书馆找到的。OpenCV 和 ImageMagick 的结合有助于单独提取正方形图像的插图。

![](img/cd1cabcc254301188225e17028d25650.png)

[Cuni]然后用数据集运行了一个 DCGAN，在对纪元和设置进行了一些修补后，生成了第一组准甲虫。在第一次实验失败后，他和 StyleGAN 一起在 [PaperSpace](https://www.paperspace.com/ml) 用 1 个 GPU 搭建了一台机器，并在 128 个 px 图像上运行了> 3 天的训练。结果好得多，但相当小，运行机器的成本相当昂贵(> €125)。![](img/2dd0ae1868533bccfdbcefd5c5db0a4e.png)

鉴于之前实验的成功，他决定转移到 [Google CoLab](https://www.google.com/url?cad=rja&cd=1&esrc=s&q=&rct=j&sa=t&source=web&uact=8&url=https%3A%2F%2Fcolab.research.google.com%2F&usg=AOvVaw3A5aPK2kLFzKOzb6sOckVw&ved=2ahUKEwidmdGN7s7mAhXNz4UKHa42DK0QFjAAegQIEBAC) ，免费使用他们每次运行 12 小时的 K80 GPU 来生成更多的甲虫。为了生产更多的 HD 甲虫，他使用了在 1024 只 px 甲虫上训练的[跑道](https://runwayml.com/)，在 3000 步后发现了更好的结果。这个模型被转移到 Google CoLab 来制作高清输出。

从那以后，他继续用甲虫做实验，制作了一些令人困惑的合成图像和有趣的 T2 收藏品。

看看这里的甲虫:

 [https://www.youtube.com/embed/NstDaqrQMDw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NstDaqrQMDw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

