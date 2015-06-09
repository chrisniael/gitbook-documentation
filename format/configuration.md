# 配置

所有的配置都以JSON格式存储在名为 `book.json` 的文件中。

你可以粘贴你的 `book.json` 去 [jsonlint.com](http://jsonlint.com/) 验证JSON语法。

## 字段

#### gitbook

```js
{ "gitbook": ">=2.0.0" }
```

这个选项是用来探测用来生成书本的GitBook的版本的。格式是一个 [SEMVER](http://semver.org/) 条件。

在 **gitbook.com** 中，这个值是根据平台中输入的标题定义的。

#### description

```js
{ "description": "This is such a great book!" }
```

这个选项定义了书本的描述，默认是从 **README**（第一段）中提取的。

在 **gitbook.com** 中，这个值是根据平台输入的描述定义的。

#### isbn

```js
{ "isbn": "978-3-16-148410-0" }
```

这个选项定义了你书本的ISBN。

#### language

```js
{ "language": "fr" }
```

这个选项定义了你书本的语言，默认值是 `en`。

这个值是用来做国际化和本地化的，它改变网站的文字。

在 **gitbook.com** 中，这个值是根据探测到的语言或指定的设置定义的。

#### direction

```js
{ "direction": "rtl" }
```

这个选项是用来重新设置语言的文字方向的。建议将 `language` 字段设置为带有正确的文字方向的语言。

#### styles

这个选项是用来自定义书本的css的。

例子：

```js
{
    "styles": {
        "website": "styles/website.css",
        "ebook": "styles/ebook.css",
        "pdf": "styles/pdf.css",
        "mobi": "styles/mobi.css",
        "epub": "styles/epub.css"
    }
}
```

#### plugins

```js
{ "plugins": ["mathjax"] }
```

书本使用的插件列表被定义在 `book.json` 的配置中。

#### pluginsConfig

```js
{
    "plugins": ["myplugin"],
    "pluginsConfig": {
        "myPlugin": {
            "message": "Hello World"
        }
    }
}
```

#### structure

这个选项是用来覆盖GitBook使用的路径的。

例如你想要使用 `INTRO.md` 代替 `README.md`：

```js
{
    "structure": {
        "readme": "INTRO.md"
    }
}
```

#### variables

```js
{
    "variables": {
        "myTest": "Hello World"
    }
}
```

这个选项定义在 [模板](./templating.md) 中使用的变量值。
