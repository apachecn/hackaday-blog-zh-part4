# “DB”=简化的微控制器调试

> 原文：<https://hackaday.com/2018/12/20/db-abbreviated-microcontroller-debugging/>

我们都经历过。当调试一个微控制器项目时，我们只想放入一个 *print* 语句来实时了解微控制器发生了什么。然而，高级嵌入式程序员知道 *printf* 语句是*禁止的:*它们太慢了。虽然没有完全解决这个困境，但[Atakan Sarioglu]想出了一个聪明的方法来用最小的运行时开销创建可读的调试消息[。](http://www.atakansarioglu.com/how-to-debug-microcontroller-printf-tool-bigbug-event-debugger/)

[Atakan Sarioglu]的创新被称为 BigBug ( [Github](https://github.com/atakansarioglu/bigbug) )，是一种动态生成的码本。密码本将通过串行(此处为 UART)发送的缩写信息转换为更长形式的人类可读信息。为了生成密码本，BigBug 会自动解析您的注释，在缩写和长格式消息之间创建一个查找表。当您在微控制器上运行程序时，BigBug 会在您通过串行发送日志/调试数据时实时将短代码转换为长消息。

比如(不限于 Arduino-only)，如果你写`Serial.println("HW") //@BB[HW] Hello World!`，BigBug 会把收到的字符`HW\n`翻译成`Hello World!`。在这个简单的例子中，缩写使用 3 个字符，而完全可读的消息使用 13 个字符，在不损失清晰度的情况下节省了大约 75%。更高级的用法让你记录数据:`Serial.println("DT 1 1") //@BB[DT] Today's Date is: {0}/{1}`变成了`Today's Date is 1/1`。您也可以使用枚举变量(最后一个例子可以用相同的 print 命令显示`Today's Date is Jan. 1`)。

就现实世界的好处而言，使用 115200 波特连接(8N1 编码)，这是 115200 比特每秒/(8+1)比特每字节= 12800 字节/秒=每 80 微秒 1 字节。发送 13 个字节的`Hello World!\n`(在简单的阻塞式 UART 实现中)需要大约 1 ms 的 CPU 时间。使用短码`HW\n`，发送基本相同的消息需要大约 0.25 毫秒(然后被 BigBug 解码)。注意，因为这只是对串行数据进行操作，所以 BigBug 是独立于语言的

如果您在调试时受到串行吞吐量的限制，这看起来是解决您的问题的一个非常好的工具。如果你只是使用 Arduino，吞吐量不成问题，那么[试试这个工具调试 Arduino 程序](https://hackaday.com/2018/11/07/debugging-arduino-is-painful-this-can-help/)。或者你可以加倍努力，然后[用一个微控制器调试另一个微控制器](https://hackaday.com/2018/02/07/debugging-an-arduino-with-an-arduino/)。