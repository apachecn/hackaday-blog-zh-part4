# 使用 SQL Lint 第一次就获得正确的 SQL 语句

> 原文：<https://hackaday.com/2020/08/18/get-your-sql-statements-right-the-first-time-with-sql-lint/>

您第一次尝试就获得 SQL 语句的平均成功率是多少？在最好的情况下，您修补了一个没有副作用的简单语句，只需要用正确的语法再试一次，或者从表名中删除输入错误，但是这里很容易出错。但是不要担心，快速修复它的日子可以结束了，这要感谢为 SQL T1 编写了 linter 的 Joe Reynolds。

linter 解析代码来告诉你哪里出错了。虽然检查 SQL 语法本身有些简单，但[Joe]的`sql-lint`工具还会通过查找实际的数据库并对其执行健全性检查来检查它的语义。目前支持 PostgreSQL 和 MySQL，它可以在单个 SQL 文件或文件目录上运行，也可以直接从命令行接受输入。更好的是，它还集成在你选择的编辑器中——假设它支持外部插件——并且[文档](https://sql-lint.readthedocs.io/en/latest/index.html)展示了如何专门为 Vim 做这件事[。](https://sql-lint.readthedocs.io/en/latest/files/configuration.html#editor-integration)

如果你能忽略它是用 TypeScript 编写的，并因此产生一个相当大的可执行文件( [~40 MB](https://github.com/joereynolds/sql-lint/releases) )的事实，它可能会成为语言本身的一个有趣的起点，或者为编写[这种类型的分析器](https://hackaday.com/2018/12/12/warnings-on-steroids-static-code-analysis-tools/)增加一个新的视角。如果数据库不适合你，【shell 脚本怎么样？

[![sql-lint in action](img/15c3ef07dce02c08d183a905754b1a7b.png)](https://hackaday.com/wp-content/uploads/2020/08/sql-lint-in-action.gif)

Example use of sql-lint