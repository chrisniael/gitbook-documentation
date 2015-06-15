# 安装ebook-convert

生成电子书 (epub, mobi, pdf) 时需要ebook-convert。

## Mac

下载 [Calibre.app](http://calibre-ebook.com/download)。移动 `calibre.app` 到你的应用程序文件夹中后，给 `ebook-convert` 工具创建一个符号链接。

```
$ sudo ln -s ~/Applications/calibre.app/Contents/MacOS/ebook-convert /usr/bin
```

你可以把 `/usr/bin` 替换为 `$PATH` 中的任何的文件夹。
