# 搜索GitBook

你可以使用[我们强大的搜索工具](https://www.gitbook.com/search)来在GitBook的上千本书中查找你需要的内容。

当你搜索GitBook的时候，你可以构造一个匹配指定数字和单词的查询语句。

## 查询文字

GitBook默认会使用查询中的关键字来搜索书本。例如 `javascript angular` 会返回所有包含单词"javascript"和"angular"的书本。

## 排除结果中特定的单词

你同样可以通过 `NOT` 语法排除单词来缩小你的搜索结果。搜索 `Hello` 会返回一大堆"Hello World"的项目，但是把搜索语句改成 `hello NOT world` 则会返回更高少的结果。

## 查询特定域的值

你可以通过指定一个特定域的值来筛选书本。例如：[license:apache-2](https://www.gitbook.com/search?q=license%3A%22apache-2%22) 会返回所有使用 Apache 2 许可证的书本。

## 查询小于/大于某个数字的值

你可以分别使用 `>` 和 `>=` 来表示 "大于" 和 "大于等于"。 例如，下面的搜索查询是等价的：`cats stars:">10"` 和 `cats stars:">=11"`

你可以分别使用 `<` 他 `<=` 来表示 "小于" 和 "小于等于"。
