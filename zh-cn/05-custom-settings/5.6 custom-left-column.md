# 自定义左栏系统文件夹

<!--
Author: amoblin
create time: 2015-08-14 06:00:10

This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建
-->

能够在用户配置文件(详见[5.1 配置文件介绍](./config-file.html))中设置如下系统文件夹：

- 最近打开的
- 配置文件

系统默认会隐藏 **配置文件** 文件夹，显示 **最近打开的** 文件夹，可通过修改行尾的 **true** 或 **false** 来控制文件夹的显示和隐藏：

```json
    "show_media_dir": false,
    "show_recent_files_dir": true,
```

