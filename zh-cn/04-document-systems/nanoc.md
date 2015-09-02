# Nanoc设置

<!-- create time: 2015-08-07 06:15:39  -->

<!-- This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建 -->

一共两步，首先生成HTML文件，其次在配置文件中配置路径。

最后会有一个示例。

## 生成HTML

如果已经生成了HTML，请略过这一步。

打开终端，进入到 nanoc文档目录， 输入 **nanoc** 回车运行来生成HTML文件。

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
    "path": "<nanoc Document Source Path>",
    "replace_with": "<nanoc Document Build HTML Path>",
    "server": "nanoc"
}
```

其中各个key说明如下：

- *path* nanoc源文件根目录路径，可以省掉Marboo主目录。
- *replace_with* nanoc生成的HTML文档根目录路径，可以省掉Marboo主目录。
- *server* 文档类型，这里写 *nanoc*

## 示例

```json
{
    "path": "/Users/amoblin/Marboo/BlogWikiDemo/nanoc-tutorial/content",
    "replace_with": "/Users/amoblin/Marboo/BlogWikiDemo/nanoc-tutorial/output",
    "server": "nanoc"
}
```

