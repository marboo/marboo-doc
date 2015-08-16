# 自定义目录浏览器(左栏文件夹的打开方式)

<!--
Author: amoblin
create time: 2015-08-07 06:44:14

This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建
-->

打开偏好设置，点击Config File中的文件路径，会打开配置文件 **marboo_config.json**，
找到如下内容：

```json
    "comment": "设置目录浏览器。可以设置Default(或者写Finder也可，都代表用Finder打开)或Terminal等",
    "folder_viewer": "Finder",
    "1.folder_viewer": "Default",
    "2.folder_viewer": "Terminal",
```
在想要的目录浏览器那一行中，删除掉key中的序号，同时把之前的key改掉。比如希望用Terminal来打开，就修改为：

```json
    "comment": "设置目录浏览器。可以设置Default(或者写Finder也可，都代表用Finder打开)或Terminal等",
    "0.folder_viewer": "Finder",
    "1.folder_viewer": "Default",
    "folder_viewer": "Terminal",
```

保存即生效。使用o或双击目录时就会使用新设定的目录浏览器来打开了。当焦点在左栏时，Marboo左下角会显示设定的目录浏览器的图标。

另外也内置了快捷键 **t** 来使用Terminal打开当前目录，方便终端用户。

