# 内容引用

内容参考 (conref) 是便于用来重复使用其他文件和书本内容。

## 导入本地文件

使用 `include` 标签导入其他文件的内容真的很简单：

```
{% include "./test.md" %}
```

## 从其他书本导入文件

GitBook 同样能处理使用了git协议的include路径：


```
{% include "git+https://github.com/GitbookIO/documentation.git/README.md#0.0.1" %}
```

git的url格式是：


```
git+https://user@hostname/project/blah.git/file#commit-ish
```

真实的git url应该以 `.git` 结尾，导入的文件名从 `.git` 之后的url片段提取。

`commit-ish` 可以是任何可以作为 `git checkout` 参数的标签，sha，或分支。默认是 `master`。

## 继承

模板继承是一种重复使用模板的简单方式。当写完一个模板，你可以定义 "block" 让字模板来替换。继承链可以任意长。

`block` 在模板中定义了一个区域并用一个名字标识了它。基类模板可以指定一些块，而子类可以用新的内容替换它们。

```
{% extends "./mypage.md" %}

{% block pageContent %}
# This is my page content
{% endblock %}
```

在文件 `mypage.md` 中，你应该指定用来替换内容的块。

```
{% block pageContent %}
This is the default content
{% endblock %}

# License

{% import "./LICENSE" %}
```
