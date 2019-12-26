# 生成静态页面

## 使用gh-pages分支

使用build命令生成静态页面

```
gitbook build
```
执行此命令后会在目录中生成_book文件夹，文件夹中便是静态页面文件，
我们可以将全部文件提交至master分支，然后执行以下命令将静态页面推送至gh-pages分支。

```
git subtree push --prefix=_book origin gh-pages
```

此种方式可以将静态页面与源文件彻底分开，但是如果内容更新，管理分支较麻烦。

## 使用master 分支的 /docs 目录

使用此种方式部署时需要指定生成静态页面的目录，命令如下

```
gitbook build ./ ./docs
```

使用此种方式在本地部署时需要变更serve命令如下

```
gitbook serve ./ ./docs
```