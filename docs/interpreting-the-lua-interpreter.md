# 重新解释 Lua 解释器

> 原文：<https://hackaday.com/2022/11/26/interpreting-the-lua-interpreter/>

Lua 背后的想法是美好的。简洁明了的语法几乎提供了一流语言的所有优点。此外，一个带有巨型交换机的解释器的简单实现可以在一个下午实现。但是汇编是在 JIT 风格的解释器中获得良好性能的关键。所以[徐浩然]开始问自己，如果没有手卷组装，他是否能获得更好的性能，在工作几个月后，[发表了一个名为 LuaJIT 翻拍(LJR)](https://sillycross.github.io/2022/11/22/2022-11-22/) 的半成品。

目前，它支持 [Lua 5.1](https://www.lua.org/versions.html#5.1) ，在 34 个基准测试中，LJR 领先最快的 Lua Lua JIT 大约 28%，领先官方 Lua 引擎 3 倍。[浩然]提供了一个很好的解释，为这个问题提供了极好的背景和上下文。

但是总而言之，切换的代价很高，并且很难针对编译器进行优化，所以使用 [tail 调用](https://en.wikipedia.org/wiki/Tail_call)是一个合理的解决方案，但是也有一些明显的缺点。通过尾部调用，每个 case 语句都变成了一个“函数”,可以跳转到这个函数，然后从这个函数中跳转出来，而不会过多地修改堆栈或寄存器。

然而，调用约定要求保留任何被调用者保存的寄存器，这意味着您丢失了一些寄存器，因为没有办法告诉编译器这个函数被允许打破调用约定。Clang 是目前唯一提供有保证的尾调用注释(`[[clang::musttail]]`)的编译器。还有其他限制，例如要求调用者和被调用者具有相同的函数原型，以防止无限制的堆栈增长。

所以[浩然]回到绘图板，写了两个新工具:C++字节码语义描述和一个叫做 Deegen 的特殊编译器。C++字节码如下所示:

```
void Add(TValue lhs, TValue rhs) {
  if (!lhs.Is<tDouble>() || !rhs.Is<tDouble>()) {
    ThrowError("Can't add!");
  } else {
    double res = lhs.As<tDouble>() + rhs.As<tDouble>();
    Return(TValue::Create<tDouble>(res));
  }
}
DEEGEN_DEFINE_BYTECODE(Add) {
  Operands(
    BytecodeSlotOrConstant("lhs"),
    BytecodeSlotOrConstant("rhs")
  );
  Result(BytecodeValue);
  Implementation(Add);
  Variant(
    Op("lhs").IsBytecodeSlot(),
    Op("rhs").IsBytecodeSlot()
  );
  Variant(
    Op("lhs").IsConstant(),
    Op("rhs").IsBytecodeSlot()
  );
  Variant(
    Op("lhs").IsBytecodeSlot(),
    Op("rhs").IsConstant()
  );
}
```

注意，这不是 C 关键字返回。相反，有一个字节码的定义和一个实现。这个字节码被转换成 LLVM IR，然后被送入 Deegen，Deegen 可以转换函数来正确地进行尾部调用，使用 GHC 调用约定，以及其他一些优化，比如通过一个巧妙的 C++ lambda 机制进行内联缓存。这篇博文写得非常好，让我们得以一窥口译员的世界。

[代码在 Github](https://github.com/luajit-remake/luajit-remake) 上。但是如果你对一个更古怪的解释器感兴趣，这里有一个用 Befunge 写的 [Brainf**k 解释器。](https://hackaday.com/2022/11/19/two-esoteric-programming-languages-one-interpreter/)