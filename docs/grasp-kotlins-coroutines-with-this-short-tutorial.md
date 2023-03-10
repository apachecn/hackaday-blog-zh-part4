# 通过这个简短的教程掌握科特林的协同程序

> 原文：<https://hackaday.com/2020/08/31/grasp-kotlins-coroutines-with-this-short-tutorial/>

Kotlin 是一种相对较新的编程语言；Java 的一个衍生物，有许多方便的小功能，比如`coroutines`。[Foalyy]正在将一个应用移植到 Android 上，同时学习 Kotlin，[在考虑了协程之后，写了一个简明的关于协程的五部分教程](https://silica.io/understanding-kotlin-coroutines/)。

Kotlin 中的协同程序是一种简化编写异步代码的方式，异步代码不一定按照编写的顺序执行。协程就像轻量级的线程，可以很容易地启动和管理，使得将阻塞和非阻塞代码连接在一起变得更加简单。(但是，协程不是线程。它们更类似于挂起一起运行得很好的函数。)

[Foalyy]发现关于协程的官方 Kotlin 文档详细描述了协程的工作原理，但是想要一个更自下而上的方法来理解它们是如何工作和使用的。幸运的是，对任何有同样想法的人来说，[Foalyy]写了这一切，并以一个重要元素的伟大回顾开始，但如果你喜欢，你可以[直接跳到例子](https://silica.io/understanding-kotlin-coroutines/5/)。

Kotlin 已经存在了一段时间，记忆力强的读者可能还记得它在这篇关于什么是神经网络以及它们如何工作的精彩介绍中的特色。