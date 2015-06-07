# 自述和介绍

书本的第一页内容是从文件 `README.md` 中提取的。如果这个文件名没有出现在 `SUMMARY` 中，那么它会被添加为章节的第一个条目。

## 使用其他文件替代README.md

一些托管在GitBook上的书更加喜欢将README.md文件作为项目的介绍而不是书的介绍。

从GitBook `>2.0.0` 起，就可以在 `book.json` 中定义某个文件作为README。

```json
{
    "structure" : {
        "readme" : "myIntro.md"
    }
}

```
