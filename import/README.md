# 导入文档

将文档导入 GitBook 很简单。当你创建一本新书的时候，使用 `Import` 标签页就可以上传文档。

## 支持的格式

| 类型 | 后缀名 |
| ---- | ------ |
| Microsoft Word 文档 | `.docx` |
| DocBook v5.x        | `.xml`  |
| HTML 文件           | `.html` |

为了充分使用它的特性，我们推荐你使用：
* Microsoft Word 2007+ 文档
* DocBook v5.x 文档

If you have existing DocBook documents in version 4, consider [converting it automatically](http://doccookbook.sourceforge.net/html/en/dbc.structure.db4-to-db5.html) to version 5 for optimized compatibility.
如果你有 DocBook v4.x 的文档，可以考虑将它们 [转化](http://doccookbook.sourceforge.net/html/en/dbc.structure.db4-to-db5.html) 成 DocBook v5.x 来解决兼容性问题。

## 转化

导入文档的特性使用了 [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) 命令行程序。这个组件负责将原始文档转化到 makrdown 文件，以及 `SUMMARY.md` 的创建。

[gitbook-convert](https://github.com/GitbookIO/gitbook-convert) 根据文章的结构，将文章划分成章节和子章节。因此，原始文档的一级标题都会被转化成一个章节。如果一个章节包含二级标题，则会为这个章节创建一个目录来包含每个子章节。

在章节目录里，会创建一个包含章节前言的 `README.md` 文件。第一个二级标题前的所有内容会被认为是一个章节的前言。这样的规则同样适用于第一个一级标题前的所有内容，它们会成为为书的前言。

对于 `.docx` 文档，[gitbook-convert](https://github.com/GitbookIO/gitbook-convert) 会将文档包含的所有图片导出到 `assets/` 目录中。

如果你需要更多的灵活性，可以考虑在本地使用 [gitbook-convert](https://github.com/GitbookIO/gitbook-convert)，然后用 Git 或 GitHub 新建一个仓库并导入转化后的内容。

## 疑难解答

我们很愿意帮忙解决你在使用 GitBook 时遇到的问题。你可以在 [github.com/GitbookIO/gitbook-convert](https://github.com/GitbookIO/gitbook-convert/issues) 提问或标注一个问题。
