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
