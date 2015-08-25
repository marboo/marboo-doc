# GitBook文档设置

<!-- create time: 2015-08-03 07:34:57  -->

<!-- This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建 -->

一共两步，首先生成HTML文件，其次在配置文件中配置路径。

最后会有一个示例。

## 生成HTML

如果已经生成了HTML，请略过这一步。

打开终端，进入GitBook文档所在目录，输入 `gitbook build` 回车运行。如果没有 `gitbook`命令，参考文末的介绍来安装gitbook。

要确保运行成功，生成了需要的HTML文件。

## 配置路径

打开自定义配置文件，找到如下内容：

```json
"comment": "For GitBook/Sphinx/VimWiki Source Files",
"url_mappings": [{
    "path":"",
    "server": ""
}],
```

添加一个url mapping，如下：

```json
{
    "path": "<GitBook Document Source Path>",
    "server": "GitBook"
}
```

如果无法显示，请显式指明html路径：

```json
{
    "path": "<GitBook Document Source Path>",
    "replace_with": "<GitBook Document Build HTML Path>",
    "server": "GitBook"
}
```

其中各个key说明如下：

- *path* GitBook源文件根目录路径，可以省掉Marboo主目录。
- *replace_with* GitBook生成的HTML文档根目录路径，可以省掉Marboo主目录。
- *server* 文档类型，这里写 *GitBook*

## 示例

这是Marboo自带的用户手册中文版的GitBook配置：

```json
{
    "path": "/Guide.localized/zh_CN.localized",
    "server": "GitBook"
}
```

也可以显式指明HTML路径：

```json
{
    "path": "/Guide.localized/zh_CN.localized",
    "replace_with": "/Guide.localized/zh_CN.localized/_book",
    "server": "GitBook"
}
```

效果如下：

![](.images/marboo-gitbook.png)

---

如果没有安装GitBook的话，参考下面。

# 安装GitBook

gitbook命令行工具是用node.js开发的，所以首先需要安装node.js环境，然后通过npm来安装gitbook。

1. 安装node.js环境，请到 [nodejs](http://nodejs.org/download/) 官网进行下载安装。也可以直接使用Homebrew来安装：

```sh
brew install node
```

2. 安装gitbook

```sh
npm install -g gitbook-cli
```
