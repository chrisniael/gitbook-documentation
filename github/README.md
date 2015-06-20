# 集成GitHub

GitBook完美的集成了 [GitHub](https://github.com/) 来托管你书本的源代码。

## 连接你的账号/权限

在集成你的书本和GitHub前，你需要授予GitBook访问你的GitHub账号的权限。

在你的 [账号设置](https://www.gitbook.com/settings) 里，使用正确的权限连接你的GitHub账号：

* __默认的权限__：仅仅在登陆的时候访问你的GitHub账号来验证你
* __访问webhook__：访问你的GitHub账号来在指定的仓库中创建webhook（查看[webhooks](#webhooks)）
* __访问公开的仓库__：从网页编辑器中访问你的GitHub仓库，你可以很容易的在GitBook中编辑你的书本（仅仅公共仓库）
* __访问私有的仓库__：和上面一项目一样，但是只能访问私有仓库

## Webhooks

当你的GitHub的仓库改变时，Webhooks会通知GitBook。

如果你的GitHub仓库改变时，GitBook没有收到通知，这个问题的主要原因是webhook。你可以检查仓库设置中webhook的状态。

## 连接书本和GitHub仓库

当你的GitHub账号正确地连接到你的GitBook账号后，将一本书链接至一个仓库很简单。

**警告**：当你在你书本的设置中指定了一个GitHub仓库，这个仓库会优先于GitBook的git仓库，这意味着编辑器会直接编辑GitHub中的内容。

1. 打开你书本设置中的GitHub部分
2. 输入你的仓库id（例如：YourGitHubUserName/RepoName）
3. 保存你的设置
4. 点击**Add a deployment webhook**按钮

你现在使用网页编辑器来编辑你的GitHub仓库（如果你授权了正确的权限）,并且你在GitHub上的提交会触发GitBook来构建书本。

## 常见的错误

**书本没有被更新/没有任何的构建**

如果你连接了你的GitHub仓库至一个GitBook项目，但是编辑它的内容却没有触发GitBook任何的构建操作。验证webhook被正确的添加到了你的GitHub仓库中（GitHub仓库设置->Webhook），如果webhook不存在或无效，之后添加它到你书本的设置中。

**改变书本的拥有者**

如果你把你的书本转移给了新的拥有者，之前的wehook会失效，你需要之后重新添加它。
