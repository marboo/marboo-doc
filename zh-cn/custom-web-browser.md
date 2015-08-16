# 自定义网页浏览器

<!--
Author: amoblin
create time: 2015-08-07 06:46:13

This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建
-->

在自定义配置文件 **marboo_config.json** 中找到如下内容：

```json
    "comment": "设置网页浏览器。Default代表默认浏览器，也可以设置已安装的浏览器如Google Chrome, Firefox等",
    "web_browser": "Default",
    "1.web_browser": "Google Chrome",
    "2.web_browser": "Firefox",
    "3.web_browser": "Safari",
    "4.web_browser": "QQBrowser",
```

在想要的浏览器那一行中，删除掉key中的序号，同时把之前的key改掉。比如希望用Firefox来打开，就修改为：

```json
    "comment": "设置网页浏览器。Default代表默认浏览器，也可以设置已安装的浏览器如Google Chrome, Firefox等",
    "0.web_browser": "Default",
    "1.web_browser": "Google Chrome",
    "web_browser": "Firefox",
    "3.web_browser": "Safari",
    "4.web_browser": "QQBrowser",
```

保存即生效。在右栏使用o就会使用新设定的网页浏览器来打开了。当焦点在右栏时，Marboo左下角会显示设定的网页浏览器的图标。

