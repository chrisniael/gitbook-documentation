## 常见错误

下面是常见错误的列表以及对应的修复方法。

---

```
Error loading plugins: plugin1, ...
```

发生这个错误是因为不能解析这个插件（或者这个插件是无效的）。外部插件需要使用 `gitbook install` 来安装。

一些插件不能加载的原因还有可能是因为他们需要另外一个版本的GitBook。如果是这样的话，你需要找到正确的插件版本来支持你使用的GitBook版本，并在 `book.json` 中定义它。

```json
{
	"plugins": ["myPlugin@1.2.3"]
}
```

---

```
Need to install ebook-convert from Calibre
```

当你尝试把你的项目构建成为PDF，ePub或者mobi格式的电子书时，为了避开错误，你必须安装了 [Calibre](http://calibre-ebook.com/) 电子书阅读/管理器和命令行工具。

从Mac版的Calibre安装命令行工具时，从菜单中选择：**calibre - Preferences - Miscellaneous - Install command line tools**

一旦完成了这个，你的电子书就会构建成功。

---
