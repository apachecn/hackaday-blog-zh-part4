# EasyOCR 让 OCR 变得简单

> 原文：<https://hackaday.com/2020/07/09/easyocr-makes-ocr-well-easy/>

在嵌入式系统上工作曾经更容易。您有一个微控制器，可能还有几个模拟或数字 I/O，通信可能是一个串行端口。今天，你的系统有网络、摄像头和大量 I/O。摄像头很奇怪，因为有时你只是想要一个图像，有时你想以某种方式理解图像。如果理解图像需要阅读图片中的文字，你会想要检查一下 [EasyOCR](https://github.com/JaidedAI/EasyOCR) 。

Python 库利用了其他开源库，并支持 42 种不同的语言。顾名思义，使用它相当容易。设置如下:

```

import easyocr
reader = easyocr.Reader(['th','en'])
reader.readtext('test.jpg')

```

结果包括定义每段文本的边界框、文本和置信度的四个点。该代码利用了 GPU 的优势，但是如果您愿意，您可以在纯 CPU 模式下运行它。还有一些其他选项，包括设置算法的扫描行为，它如何处理多个处理器，以及它如何将图像转换为灰度。结果看起来令人印象深刻。

根据该项目的知识库，他们合并了几个现有的神经网络算法和常规算法，所以如果你想深入了解细节，可以提供代码和白皮书的链接。如果你需要一些关于如何使用 OCR 的灵感，也许这个[过去的项目](https://hackaday.com/2016/03/21/mobile-text-reader-with-ocr-and-text-to-speech/)会给你一些想法。或者你可以[在游戏中作弊](https://hackaday.com/2014/03/24/bookworm-playing-bot-tests-programmers-ocr-skills/)。