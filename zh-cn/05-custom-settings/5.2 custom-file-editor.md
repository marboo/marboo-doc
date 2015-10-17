# 自定义文件编辑器

## 最简单的方式：打开偏好设置，可以设置编辑器，如图：

![](http://marboo.io/.media/marboo.io/images/marboo-editor.png)

或者 打开用户配置文件(详见[5.1 配置文件介绍](./config-file.html))，找到如下内容：

```json
    "comment": "设置文件编辑器。Default(或者写Finder也可)代表Finder中关联的编辑器，也可以设置已安装的编辑器如 Emacs, MacVim, TextMate, Mou等",
    "file_editor": "Default",
    "0.file_editor": "Do as Finder do",
    "1.file_editor": "Finder",
    "2.file_editor": "Emacs",
    "3.file_editor": "MacVim",
    "4.file_editor": "Atom",
    "5.file_editor": "Mou",
    "6.file_editor": "Sublime Text",
    "7.file_editor": "TextMate",
```

在想要的编辑器那一行中，删除掉key中的序号，同时把之前的key改掉。比如希望用Emacs来打开，就修改为：

```json
    "comment": "设置文件编辑器。Default(或者写Finder也可)代表Finder中关联的编辑器，也可以设置已安装的编辑器如 Emacs, MacVim, TextMate, Mou等",
    "0.file_editor": "Default",
    "0.file_editor": "Do as Finder do",
    "1.file_editor": "Finder",
    "file_editor": "Emacs",
    "3.file_editor": "MacVim",
    "4.file_editor": "Atom",
    "5.file_editor": "Mou",
    "6.file_editor": "Sublime Text",
    "7.file_editor": "TextMate",
```

保存即生效。使用o或双击文件名时就会使用新设定的文件编辑器来打开了。当焦点在中栏时，Marboo左下角会显示设定的文件浏览器的图标。

	
## 根据文件类型设置不同的编辑器

<!-- create time: 2015-08-07 06:30:21  -->

<!-- This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建 -->


如果想根据文件的属性来进行配置，则需要在用户配置文件(详见[5.1 配置文件介绍](./config-file.html))的 *rules* 字段中设置。

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

将上述内容放到 最后一行的 *The End* 之前，保存，刷新文件即生效。
