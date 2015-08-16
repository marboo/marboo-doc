# Custom Web Browser

<!--
Author: amoblin
create time: 2015-08-07 06:46:13

This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建
-->

Find the content following in *marboo_config.json* :

```json
    "comment": "设置网页浏览器。Default代表默认浏览器，也可以设置已安装的浏览器如Google Chrome, Firefox等",
    "web_browser": "Default",
    "1.web_browser": "Google Chrome",
    "2.web_browser": "Firefox",
    "3.web_browser": "Safari",
    "4.web_browser": "QQBrowser",
```
in the line contains the web browser you want to use, move the number and add number to the previous key. For Example, if you want to use Firefox to preview, modify the content to:

```json
    "comment": "设置网页浏览器。Default代表默认浏览器，也可以设置已安装的浏览器如Google Chrome, Firefox等",
    "0.web_browser": "Default",
    "1.web_browser": "Google Chrome",
    "web_browser": "Firefox",
    "3.web_browser": "Safari",
    "4.web_browser": "QQBrowser",
```

once saved, the config will be update.

