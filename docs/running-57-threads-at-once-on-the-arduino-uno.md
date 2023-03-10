# 在 Arduino Uno 上同时运行 57 个线程

> 原文：<https://hackaday.com/2021/03/17/running-57-threads-at-once-on-the-arduino-uno/>

当人们想到 Arduino Uno 时，人们会想到一个强大的 8 位微控制器平台，但它的性能并没有让世界为之惊叹。与 ESP32 等更现代的部件不同，它只有一个内核，没有真正的多任务处理能力。但是，如果想在一个 Uno 上同时运行多个线程呢？[[Adam]快速编写了一些代码来完成这个任务。](https://create.arduino.cc/projecthub/adamb314/how-to-run-57-hard-real-time-threads-on-an-arduino-uno-b8e742)

当您有多个任务需要同时完成而又不会互相干扰时，线程就非常有用。[Adam]的 [ThreadHandler 库](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa0l2Y1hHbDdMSVgyTGxRbVNUaFRBcG00Umwzd3xBQ3Jtc0trclFKcGpVSXBGTS01MkVfei1CUW1RME9rMXNueDNkbGRFSVNOQm55SXZ1MnE3MUE4dk1HWlQ3NmdsZm1hanBlckdmSjhOcmJyd3hrTXVoMlNCek91S3FacWxVT29nVWc1am9wMUw5R3RSc0dqcjNERQ&q=https%3A%2F%2Fbitbucket.org%2Fadamb3_14%2Fthreadhandler%2Fsrc%2Fmaster%2F)的神奇之处在于，它被设计成可以运行许多线程，并且是实时运行的，还带有优先级管理。在 Arduino Uno 上，当然没有速度恶魔，它可以以 6 毫秒的间隔同时运行多达 57 个线程，最小计时误差为 556 秒，最大 952 秒。在 7 个线程的更合理数量下，最小误差降至仅 120 秒。每个线程的估计开销为 1.3%的 CPU 负载和 26 字节的 RAM 使用。

当我们绞尽脑汁想我们能用 Arduino Uno 上的几个线程做些什么的时候，我们确信你可能会有一些想法——在评论中发表吧。ThreadHandler 可以在这里找到，它可以在 SAMD21 板以及任何与 TimerOne 兼容的基于 AVR 的板上运行。我们以前也见过相同领域的其他工作，[比如 Arduino 平台的 ChibiOS】。休息后的视频。](https://hackaday.com/2016/09/22/arduino-sketch-the-next-generation/)

 [https://www.youtube.com/embed/59oS82EKz9w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/59oS82EKz9w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

