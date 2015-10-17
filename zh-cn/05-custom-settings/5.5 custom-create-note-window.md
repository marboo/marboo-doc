## 自定义新建笔记的类型列表

<!--
Author: amoblin
create time: 2015-08-07 06:33:22

This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建
-->

打开用户配置文件(详见[5.1 配置文件介绍](./config-file.html))，找到如下内容进行修改：

```json
  "comment": "设置新建笔记时的笔记类型列表",
    "new_file_types": [{
        "display_name": "Markdown",
        "file_extension": "md"
    },{
        "display_name": "reStrucutred Text",
        "file_extension": "rst"
    },{
        "display_name": "Org-mode",
        "file_extension": "org"
    },{
        "display_name": "Custom",
        "file_extension": ""
    }],
```
