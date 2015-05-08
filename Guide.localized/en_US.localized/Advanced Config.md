# Custom Functions

<!-- create time: 2014-12-07 19:00:20  -->

如果想根据文件的属性来进行配置，则需要在 *rules* 字段中设置。

比如，希望将 *\*.md* 的文件使用Emacs打开，而 *\*.mkd*的文件使用MacVim打开，则配置如下：

```json
    "rules": [{
	    "file_type": "Markdown",
	    "pips": [
	    ],

        "piplines": [{
	        "filename": "*.md",
	        "editor": "Emacs",
	        "pipline": []
	    },{
	        "filename": "*.mkd",
	        "editor": "MacVim",
	        "pipline": []
        }]
    },{
    }],
```

将上述内容写到 最后一行的 *The End* 之前，保存，刷新文件即生效。

