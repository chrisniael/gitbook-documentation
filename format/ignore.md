# 忽略文件和文件夹

GitBook会读取 `.gitignore`，`.bookignore`，`.ignore` 文件来获取忽略的文件和目录的列表。

这些文件的格式，遵循和 `.gitignore` 同样的约定：

# This is a comment

# Ignore the file test.md
test.md

# Ignore everything in the directory "bin"
bin/*
```
