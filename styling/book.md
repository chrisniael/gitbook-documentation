# 扩展网站和电子书样式

你可以通过在 `styles` 目录中建立文件来扩展电子书和网站使用的css：

| 类型                  | 文件                |
|-----------------------|---------------------|
| `website`             | `styles/website.css |
| `pdf`                 | `styles/pdf.css`    |
| `epub`                | `styles/epub.css`   |
| `mobi`                | `styles/mobi`       |
| `pdf`, `epub`, `mobi` | `styles/ebook.css   |

这些路径可以在 `book.json` 设置中改变，例如使用根文件夹中的文件：

```json
{
	"styles": {
		"website": "website.css",
		"ebook": "ebook.css",
		"pdf": "pdf.css",
		"mobi": "mobi.css",
		"epub": "epub.css"
	}
}
```

## 使用 CSS 预处理

这些插件是用来让你更简单的使用 CSS 预处理：

- [styles-less](https://plugins.gitbook.com/plugin/styles-less)
- [styles-sass](https://plugins.gitbook.com/plugin/styles-sass)
