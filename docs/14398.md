# 有时候，人工智能会创建你的电子表格

> 原文：<https://hackaday.com/2022/08/09/ai-creates-your-spreadsheets-sometimes/>

我们一直有兴趣看看人工智能如何处理除了愚蠢的图像以外的东西。这就是为什么“[免费的人工智能机器人能够为任何问题](https://excelformulabot.com)生成 Excel 公式”吸引了我们的眼球。基于 GPT-3，它可以将你的问题描述转换成适合 Excel 或 Google 工作表的公式。

我们的第一个提示效果不是很好。但那是我们的错。当他们说“Excel 公式”时，他们指的是字面意思。因此，试图用列或行来描述您想要的实际结果似乎超出了它的范围。没有意识到这一点，我们问:

```
If the sum of column H is greater than 50, multiply column A by 0.33
```

得到了:

```
=IF(SUM(H:H)>50,A*0.33,0)
```

## 更好的尝试

这很接近，但即使稍微精通 Excel 的人也不会理解这个请求。但这不公平。我们认为这确实是一个 y=f(x)类的问题。

这里有一个不同的提示:

```
Negative 1 if the sum of column H is greater than 50, 
otherwise 1 unless cell A4 is negative and then the result is 42
```

结果是:

```
=IF(SUM(H:H)>50, -1, IF(A4<0, 42, 1))
```

那么智能在哪里呢？结果当然是对的，但是自己搞清楚也没那么难。

这类事情的部分问题是它们不精确。该网站否认“模型中可能存在不完善之处”和“在投入使用之前验证该输出”。验证这是正确的意味着你可以自己写，这可能不会花太多时间。

## 查找公式

我们印象深刻的是，它似乎知道如何找到某些关系。例如:

```
Find the power if the voltage is in cell B1 and the current in cell C1
=B1*C1
```

或者…

```
The current for a resistor in R1 when the voltage is in E1

=E1/R1
```

不过，有趣的是。它一定是基于细胞的实际名称，因为试试这个:

```
The current for a resistor in C5 when the voltage is in C6
```

出于某种原因，这个等式颠倒了过来:

```
=C5/C6
```

这只是表明神经网络不像我们那样思考问题。我们认为这个是对的:

```
The amount of interest on a V1 balance at a compound interest rate in P1 compounded annually for V2 years

=V1*(1+P1)^V2
```

但是我们很确定这个是错的:

```
The time it takes a ball to fall to the ground from Q1 feet

=Q1/32
```

## 我们的意见

所以，在我们看来，这只不过是一个室内把戏。您可能已经有了一些关键字匹配模板，并获得了同样好的结果，这也将是更可重复的。你甚至可以要求澄清或注意看似不可能的情况。

这个有市场吗？当然，当它成为星际迷航级别的计算机交互时。(“计算机:对所有已知的罗慕伦传输格式进行分析……”)。但在 GPT-3 从自然语言中猜测我们的公式的水平上，它只是一个玩具。即使是做得更好的 Wolfram Alpha 也不能胜任这项任务，尽管我们想知道他们推出 Excel 公式会有多难？至少它比我们一直听说的“[提示工程](https://techcrunch.com/2022/07/29/a-startup-is-charging-1-99-for-strings-of-text-to-feed-to-dall-e-2/)要好。

这并不是说 GPT-3 没有用。这显然是为了某些问题。将它用于电子表格的实现不在其中。不过，还是很整洁。

 [https://www.youtube.com/embed/6CDhEwhOm44?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6CDhEwhOm44?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

