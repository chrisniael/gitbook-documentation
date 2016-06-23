# 使用Git更新书本

当你在**gitbook.com**上创建了书本后，你需要推送一些内容给它。你可以使用网页编辑器或者命令行来做这件事。

如果你想要通过命令行来更新你的书本的话，你可以使用 [GIT](http://git-scm.com/) 来推送你的内容。

## GIT Url

每本书本都有一个相关联的Git HTTPS url。GitBook的git服务器暂时还不支持ssh协议。

git url的格式是：

```
https://git.gitbook.com/{{UserName}}/{{Book}}.git
```

## 认证

git服务器使用你基本的GitBook登录来认证你。当提示的时候，输入你的GitBook用户名和密码（你同样可以使用你的API token）。

## 保存你的凭证

To avoid having to enter your password on each new push, you can add your GitBook credentials to your `~/.netrc` file. Create or append to an existing `~/.netrc` file something like below:
为了避免每次 push 的时候输入密码，你可以将你的 GitBook 凭证添加到 `~/.netrc` 文件里。将下面内容添加到 `~/.netrc` 文件中：

```
machine git.gitbook.com
  login 用户名或邮箱
  password API-TOKEN或密码
```

为了安全起见，我们推荐你使用 **API TOKEN**，你可以在 [in your settings under "API"](https://www.gitbook.com/settings#api) 找到它。

## 在命令行创建一个新的仓库

```shell
touch README.md SUMMARY.md
git init
git add README.md SUMMARY.md
git commit -m "first commit"
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u gitbook master
```

## 推送一个已存在的仓库

```shell
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u gitbook master
```
