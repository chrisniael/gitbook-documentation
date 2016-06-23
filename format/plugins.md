# 插件

插件是扩展 GitBook 功能（电子书和网站）最好的方式。现在插件可以做很多事：支持数学公式的显示，使用 Google Analytic 追踪访问，...

## 如何查找插件？

可以在 [plugins.gitbook.com](http://plugins.gitbook.com) 上很轻松的查找插件。

## 如何安装插件？

当你找到你要安装的插件后，你需要将它们添加至 `book.json` 中：

```
{
"plugins": ["myPlugin", "anotherPlugin"]
}
```

你可以使用：`"myPlugin@0.3.1"` 来指定一个特定版本，当你使用旧版本的 GitBook 时，这个很有用。

如果你打算本地 build 你的书，可以运行 `gitbook install` 来下载和准备插件。
