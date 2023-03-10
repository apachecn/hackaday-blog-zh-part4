# 一只稳定的手让这个芯片再次工作

> 原文：<https://hackaday.com/2019/03/21/a-steady-hand-makes-this-chip-work-again/>

当你在处理一些老式 IC 时，其中一条小腿突然掉了，你会怎么做？这就是[Kotomi]在与一个旧的超级任天堂合作时发生的事情。声音芯片的一根引线突然断了，[使得【Kotomi】的工作系统](http://www.obsolete-tears.com/sauver-une-puce-dossier-119.html)([Google Translatrix](https://translate.google.com/translate?sl=fr&tl=en&u=http%3A%2F%2Fwww.obsolete-tears.com%2Fsauver-une-puce-dossier-119.html))少了一根引线。如果你有一只稳定的手和一个每分钟数千转的旋转工具，这个问题是可以解决的。

解决这个问题依赖于集成电路是如何构建的一点点知识。这里有一小块方形的硅，但是这个小芯片被粘合到一个金属引线框上，看起来像一只机器蜈蚣的胸腔。这个引线框被环氧树脂覆盖，引脚向下弯曲，这样你就有了一个集成电路。去除一点点环氧树脂就可以接触到引线框，然后就可以焊接了。不要呼吸修复，它不漂亮，但它确实有效。

虽然这种技术利用 Dremel 来打破老式芯片的耐嚼牛轧糖中心，在某些方面这可以被称为解封，但实际上不是。我们已经看到[人们滴酸](https://hackaday.com/2016/12/27/extracting-sounds-with-acid-and-uv/)到芯片的中心[一个非常热的火炬](https://hackaday.com/2017/04/07/popping-the-top-of-a-ceramic-ic/)将到达陶瓷芯片的中间，但这种技术只是访问 ic 的引线框架。所有集成电路都有一个冲压(或光刻)金属框架，硅芯片与该框架相结合。对一些环氧树脂运行 Dremel 不会访问硅，但它可以访问来自芯片的信号。