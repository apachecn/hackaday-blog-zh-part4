# Javascript 无处不在。甚至 MSDOS

> 原文：<https://hackaday.com/2022/04/15/javascript-is-everywhere-even-msdos/>

尽管专家们开玩笑说，Java 的“一次编写，到处运行”的口号可能更好地表达为“一次编写，到处调试”，但 Java 的亲戚——JavaScript——在这两个承诺上都比它的同名物做得更好。由于在浏览器中的扩散，JavaScript 是计算机语言的真正通用语言，这导致了使用 Node.js 和 Electron 等工具编写的整个应用程序，而不仅仅是浏览器。但是如果你还在用 MSDOS 或者 Windows 98 呢？我们知道你们有些人会，至少在复古机器上。不要觉得被冷落了，DOjS 项目有 [jSH，一个用于 DOS 和相关操作系统的 JavaScript 引擎](https://github.com/SuperIlu/jSH)。

为什么？我们不知道，但我们赞赏这种努力。项目主页中的示例显示了如何重命名目录中的所有文件扩展名:

```
if (args.length < 3) {
   Println("Usage:");
   Println(" jSH.exe renall.js   ");
   Exit(1);
}

var dir = args[0];
var oldExt = args[1].toUpperCase();
var newExt = args[2].toUpperCase();

var files = List(dir);
for (var i = 0; i  " + dir + "\\" + newName);
     Rename(dir + "\\" + oldName, dir + "\\" + newName);
     }
   }   
Println("All done...");
```

当然，还有一百万种其他方法可以做到这一点。另一方面，有一个包管理器——假设您有一个正常工作的网络连接，我们可以想象在一些情况下这可能有点用处。

如果你试图避开 JavaScript，你可能不得不考虑退回到 [CP/M](https://hackaday.com/2018/07/28/the-4-z80-single-board-computer-evolved/) 。或者拥抱它，在 MSDOS 上做你的下一个[逻辑模拟](https://hackaday.com/2020/11/02/ttl-simulator-in-javascript/)(也许)。