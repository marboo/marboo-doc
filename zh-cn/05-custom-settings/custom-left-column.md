# 自定义左栏系统文件夹

<!--
Author: amoblin
create time: 2015-08-14 06:00:10

This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建
-->

用户配置文件 **marboo_config.json** 中可以设置左栏的系统文件夹有：

- 最近打开的
- 配置文件

若要在左栏显示**最近打开的**文件夹，可以在**marboo_config.json**中增加如下配置：

```json
    "show_recent_files_dir": true,
```

若要在左栏显示**配置文件**文件夹，可以在**marboo_config.json**中增加如下配置：

```json
    "show_media_dir": true,
```
    
系统默认会显示 **最近打开的** 文件夹，隐藏 **配置文件** 文件夹：

```json
    "show_media_dir": false,
    "show_recent_files_dir": true,
```
    
