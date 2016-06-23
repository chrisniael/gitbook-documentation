# 数学 & Tex

GitBook 可以使用插件支持数学公式和 Tex。当前有两个官方的插件用来显示数学公式：[mathjax](https://github.com/GitbookIO/plugin-mathjax) 和 [katex](https://github.com/GitbookIO/plugin-katex)。

## 开启数学插件

为了开启数学公式支持，你需要选择（[mathjax](https://github.com/GitbookIO/plugin-mathjax) 或 [katex](https://github.com/GitbookIO/plugin-katex)）一个插件添加到 `book.json` 中：

```js
{
    "plugins": ["mathjax"]
}
```

## MathJax 和 KaTeX 的区别

`mathjax` 和 `katex` 插件是 Tex 公式绘制的不同实现，它们基于各自的开源库：[KaTeX](https://github.com/Khan/KaTeX) 和 [MathJax](https://www.mathjax.org) 。

MathJax 支持整个 Tex 语法，但是在制作电子书版本时不是很完美。
KaTex 在所有格式（网页和电子书）的绘制上都很完美，但是还不支持 [所有的语法](https://github.com/Khan/KaTeX/wiki/Function-Support-in-KaTeX)。


## 添加数学公式

```
这里是一些内嵌的数学公式：$$a \ne 0$$
```

数学公式块需要另起新行：

```
这里是一个数学公式块

$$
a \ne 0
$$
```
