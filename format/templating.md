# 模板

这是GitBook可使用的模板特性的简要概述。GitBook使用 [Nunjucks](https://mozilla.github.io/nunjucks/) 和 [Jinja2](http://jinja.pocoo.org/) 的语法。

## 转义

如果你想要输出任何特殊的目标标签，你可以使用raw，任何在其中的内容都会原样输出。

```
{% raw %}
  这 {{ 不会被处理 }}
{% endraw %}
```

## 变量

变量会从书本内容中寻找对应的值。

变量被定义在 `book.json` 文件中：

```json
{
    "variables": {
        "myVariable": "Hello World"
    }
}

#### 显示变量

定义在 `book.json` 中的变量可以在 `book` 作用域下被访问：

```
{{ book.myVariable }}
```

这会从书本的变量中寻找 `myVariable` 并显示它。变量的名字可以存在点 (dot) 来查找属性。你同样可以使用方括号语法。

```
{{ book.foo.bar }}
{{ book["bar"] }}
```

如果对应的值没有定义，那么什么也不会显示。下面这些语句不会输出任何东西，如果 `foo` 没有定义的话：`{{ book.foo }}`，`{{ book.foo.far }}`，`{{ book.foo.bar.baz }}`。

#### 上下文变量

一些变量也可以用来获取当前文件或GitBook实例的信息。

| Name | Description |
| ---- | ----------- |
| `file.path` | Path of the file relative to the book |
| `file.mtime` |Last modified date of the file |

## 标签

标签是在章节和模板中执行操作的特殊块

#### If

**if** 测试一个条件并让你选择性的显示内容。它的行为的和编程语言中的if一样。

````
{% if variable %}
  It is true
{% endif %}
```

如果 `variable` 被定义了并且是真的，那么 "It is true" 就会被显示出来。否则，没有任何东西会被显示。

你可以使用elif和else来指定选择性条件：

```
{% if hungry %}
  I am hungry
{% elif tired %}
  I am tired
{% else %}
  I am good!
{% endif %}
```

#### for

**for** 迭代数组和字典。

让我们来看一下 `book.json` 中的变量：

```
{
    "variables": {
        "authors": [
            { "name": "Samy" },
            { "name": "Aaron" }
        ]
    }
}
```


```
# Authors


{% for author in book.authors %}
  - {{ author.name }}
{% endfor %}
```

上面的例子使用 `authors` 数组的每项的 `name` 属性作为显示的值，列出了所有的作者 (author) 。

#### include

Include 的详细描述在文章 [内容引用](./conrefs.md) 中。
