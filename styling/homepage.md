# 主页主题

主题可以使用预定义或自定义的HTML模板来定制你**gitbook.com**上书本的主页。

## 预定义的主题

GitBook预定义主题是开源的并可以从[GitHub](https://github.com/GitbookIO/themes)获取。

### 书本主页的变量

|  变量  |     类型 |     描述     |
|--------|----------|--------------|
| `book` | `<book>` | 要显示的书本 |

### 书本的表示

| 变量                 | 类型            | 描述                                       |
|----------------------|-----------------|--------------------------------------------|
| `id`                 | `string`        | 书本的完整的id（例如：`Username/Test`）    |
| `name`               | `string`        | 书本的名字                                 |
| `title`              | `string`        | 书本的标题                                 |
| `description`        | `string`        | 书本的描述                                 |
| `public`             | `boolean`       | 书本是私有的则为False                      |
| `price`              | `number`        | 书本的价格（0 等价于免费）                 |
| `githubId`           | `string`        | 书本在GitHub上的ID（例如：`Username/Test`）|
| `categories`         | `array[string]` | 与书本相关的标签的列表                     |
| `author`             | `<user>`        | 创建书本的用户                             |
| `collaborators`      | `array[<user>]  | 书本的合作者的数组（不包括作者）           |
| `cover.small`        | `string`        | 封面的Url（小尺寸）                        |
| `cover.large`        | `string`        | 封面的Url（大尺寸）                        |
| `urls.access`        | `string`        | 书本主页的Url                      |
| `urls.homepage`      | `string`        | 主页的Url（使用定制的域名）                |
| `urls.read`          | `string`        | 阅读书本的Url                              |
| `urls.reviews`       | `string`        | 评论页面的Url                              |
| `urls.subscribe`     | `string`        | 提交邮件订阅的Url                          |
| `urls.download.epub` | `string`        | 下载电子书的Url（EPUB格式）                |
| `urls.download.mobi` | `string`        | 下载电子书的Url（Mobi格式）                |
| `urls.download.pdf`  | `string`        | 下载电子书的Url（PDF格式）                 |

### 用户的表示

| 变量               |     类型 | 描述                               |
|--------------------|----------|------------------------------------|
| `username`         | `string` | 用户的用户名                       |
| `name`             | `string` | 用户的的名字                       |
| `urls.profile`     | `string` | 主页设置的Url                  |
| `urls.avatar`      | `string` | 头像的Url                          |
| `accounts.twitter` | `string` | Twitter上的用户名（如果关联了的话）|
| `accounts.github`  | `string` | GitHub上的用户名（如果关联了的话） |
