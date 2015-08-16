# Gollum设置

<!-- create time: 2015-08-07 06:20:04  -->

<!-- This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建 -->

一共两步，首先运行Gollum Server，其次在配置文件中配置路径。

最后会有一个示例。

## 运行Gollum Server

在终端下进入**Gollum Path**目录，执行 **gollum .** 来启动Gollum Server。

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
    "path": "<Gollum Document Source Path>",
    "port": "<Gollum Server Port",
    "server": "Gollum"
}
```

其中各个key说明如下：

- *path* Gollum源文件根目录路径，可以省掉Marboo主目录。
- *port* Gollum Server端口号，默认是4567。
- *server* 文档类型，这里写 *Gollum*


## 示例

```json
{
    "path": "/CCBooks/Wikis/amoblin-wiki",
    "server": "Gollum"
}
```
