# 用 ChaiScript 给你的 C++程序添加脚本

> 原文：<https://hackaday.com/2019/07/26/add-scripting-to-your-c-programs-with-chaiscript/>

如果您正在编写一个具有技术用户基础的程序，那么让程序可脚本化是一个不错的选择。事实上，您可能希望用编程语言来完成繁重的工作，然后使用您的脚本语言来构建功能。理论上，这应该很容易。有许多嵌入式脚本库，它们为您的代码访问脚本资源和脚本资源访问选定的主机变量和函数提供了一些方法。如果你使用 C++，一个更简单的方法是使用 [ChaiScript](http://chaiscript.com/) 。

ChaiScript 是 BSD 许可的——假设您的编译器支持 c++ 14——它就像包含一个头文件和进行几个调用一样简单。不需要特殊的工具或库。代码可以在操作系统之间移植，包括 32 位和 64 位 Windows。它也是线程安全的，除非您关闭该功能。
 柴书有多简单？下面是他们公开一个函数的例子(当然是 HelloWorld)。该函数接受一个参数并返回值。主程序建立函数和脚本之间的链接，然后运行一个简单的脚本。

```
#include <chaiscript/chaiscript.hpp>

std::string helloWorld(const std::string &t_name) {
   return "Hello " + t_name + "!";
}

int main() {
   chaiscript::ChaiScript chai;
   chai.add(chaiscript::fun(&helloWorld), "helloWorld");

   chai.eval(R"(
      puts(helloWorld("Bob"));
       )");
}
```

一个真正的程序可能更倾向于从一个文件或其他用户指定的东西中读取它的脚本，但是这很容易想象。根据[文档](http://chaiscript.com/docs.html)，你的脚本可以调用 C++，而 C++可以调用脚本，并且都是以类型安全的方式。您还可以传播异常。

脚本语言本身很简单。比起正式的文档，你可能更喜欢[备忘单](https://github.com/ChaiScript/ChaiScript/blob/develop/cheatsheet.md)。例子也不少。

很容易忽略脚本语言，但是它们对于某些应用程序来说是完美的。ChaiScript 和类似的工具可以让您用最困难的方式构建困难的部分，用最简单的方式构建简单的部分。毕竟，你可能使用 bash，它只不过是一种[脚本语言](https://hackaday.com/2018/06/29/linux-fu-scripting-for-binary-files/)。