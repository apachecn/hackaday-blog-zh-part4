# 用简单的英语编程

> 原文：<https://hackaday.com/2020/06/12/programming-in-plain-english/>

《星际迷航》有非常智能的电脑，你可以简单地告诉他们你想做什么，他们就做了。[Rzeppa]家族已经启动了一个简单英语编译器。它在 Windows 下运行，看起来相当有能力。

简单语言编程并不是一个新的想法。COBOL 应该模仿自然语言，使用如下语句:

```
MULTIPLY HOURS BY RATE GIVING PAYAMOUNT
```

你可能会说这不是很好，但是在商业世界中仍然有很多 COBOL 在做很多事情。今天的计算机有更多的内存和速度，所以程序员几十年来变得越来越罗嗦。不再有`X1`和`fprdx`这样的变量名。也许这个会流行起来。

一个清除屏幕的函数从一个你可能说的调用例程的短语列表开始。这类似于个人助理逻辑的类型，其中你可以说自然语言，但在这样做时，你最好说一些与其已知模板匹配的东西。函数如下:

```
To erase the screen;
To blank out the screen;
To wipe off the screen;
To clear the screen:
Unmask everything.
Draw the screen’s box with the black color and the black color.
Refresh the screen.
Put the screen’s box into the context’s box.
```

如果你说“擦除屏幕”或“清空屏幕”，这将会起作用，但如果你说“清空屏幕”，这将不起作用。附图中显示的 hello world 程序如下所示:

```
To run:
Start up.
Clear the screen.
Use medium letters. Use the fat pen.
Pick a really dark color.
Loop.
Start in the center of the screen.
Turn left 1/32 of the way.
Turn right. Move 2 inches. Turn left.
Write “HELLO WORLD”.
Refresh the screen.
Lighten the current color about 20 percent.
Add 1 to a count. If the count is 32, break.
Repeat.
Wait for the escape key.
Shut down.
```

我们感兴趣的是，一些原语允许您插入机器码。例如:

```
To add a number to another number:
Intel $8B85080000008B008B9D0C0000000103.
```

这意味着如果你感兴趣，你可以做一些有趣的扩展。如果你想尝试一下，粗略的尝试显示它在葡萄酒下确实有效——至少在一定程度上。

这篇文章的重点是让学生使用这种语言，但是我们不确定这些是未来程序员应该养成的好习惯，除非它是一种趋势的前沿。不过，我们也可以对 Scratch 和其他 T2 视觉开发工具 T3 进行同样的讨论。