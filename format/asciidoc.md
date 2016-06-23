# AsciiDoc

从 `2.0.0` 版本起，GitBook也能支持AsciiDoc作为输入的格式了。

关于这个格式的更多信息请参考 [AsciiDoc Syntax Quick Reference](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/)。

和markdown一样，GitBook也使用了一些特殊的文件来提取书本的结构：`README.adoc`，`SUMMARY.adoc` 和 `GLOSSARY.adoc`。

## README.adoc

这是书本的最重要项目：介绍。这个文件是**必须的**。

## SUMMARY.adoc

这个文件定义了章节和子章节的列表。和 [markdown](./chapters.md) 文件一样，`SUMMARY.adoc` 的格式是简单的链接列表，链接的名字是章节的名字，链接的目标是章节文件的路径。

子章节被简单的定义成添加到父章节的内嵌列表。

```
= Summary

. link:chapter-1/README.adoc[Chapter 1]
.. link:chapter-1/ARTICLE1.adoc[Article 1]
.. link:chapter-1/ARTICLE2.adoc[Article 2]
... link:chapter-1/ARTICLE-1-2-1.adoc[Article 1.2.1]
. link:chapter-2/README.adoc[Chapter 2]
. link:chapter-3/README.adoc[Chapter 3]
. link:chapter-4/README.adoc[Chapter 4]
.. Unfinished article
. Unfinished Chapter
```

## LANGS.adoc

对于 [多语言](./languages.md) 书，这个文件是用来定义支持的语言和翻译。

这个文件遵循 `SUMMARY.adoc` 一样的语法：

```
= Languages

. link:en/[English]
. link:fr/[French]
```

## GLOSSORY.adoc

这个文件是用来定义术语的。请查看 [术语表](./glossary.md) 那章节。

```
= Glossary

== Magic
Sufficiently advanced technology, beyond the understanding of the observer producing a sense of wonder.

== PHP
+A popular web programming language, used by many large websites such as Facebook. Rasmus Lerdorf originally created PHP in 1994 to power his personal homepage (PHP originally stood for "Personal Home Page" but now stands for "PHP: Hypertext Preprocessor").
```
