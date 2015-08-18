# Custom Folder Browser

<!--
Author: amoblin
create time: 2015-08-07 06:44:14

This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建
-->

Open the preference window, click the file path in "Config File", a config file named *marboo_config.json* will be opened.

find the content following：

```json
    "comment": "设置目录浏览器。可以设置Default(或者写Finder也可，都代表用Finder打开)或Terminal等",
    "folder_viewer": "Finder",
    "1.folder_viewer": "Default",
    "2.folder_viewer": "Terminal",
```
in the line contains the folder viewer which you want to sue, remove the number and add number to the previous key. For example, if you want to use Terminal to open folder, then change the content to:

```json
    "comment": "设置目录浏览器。可以设置Default(或者写Finder也可，都代表用Finder打开)或Terminal等",
    "0.folder_viewer": "Finder",
    "1.folder_viewer": "Default",
    "folder_viewer": "Terminal",
```

save the file, and the config will be updated.

BTW, you can enter <kbd>t</kbd> to open Terminal with current directory, useful for terminal user.

