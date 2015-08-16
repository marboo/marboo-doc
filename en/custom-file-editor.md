# Custom File Editor

<!-- create time: 2015-08-07 06:30:21  -->

<!-- This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建 -->

## the simple way：open preference window to change default file editor.

or find the content as following in *marboo_config.json* :

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

in the line contains the file editor you want to use, remove the number and add line number to the previous key. For example, if you want to use Emacs to edit file, then modify the content to:

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

once saved, the config will be updated.
	
## different file editor for different file

If you want to config by the file attributes, then you must config the *rules* key in **marboo_config.json**.

For example, if you want to use Emacs to open *\*.md* files, use MacVim to open *\*.mkd* files, then config as following:

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

write the content befor the line *The End*. once saved, the config will be updated.
	
