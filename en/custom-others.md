# Custom Functions
<!-- create time: 2014-12-07 19:00:20  -->

Modify **marboo_config.json** to use more features.


## custom whether init new file content from marboo template when create new file from command line

```json
    "comment": "设置对于命令下下创建的文件，是否按照Marboo配置进行初始化",
    "init_content_for_commandline": false,
```

The default value is "false". If true, when use "touch" command to crate a new file from command line, Marboo will init the file content by file type. For example: 


    ➜ $ touch test.md
    ➜ $ cat test.md
    # test

    <!-- create time: 2015-07-04 07:27:44  -->

    <!-- This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
    本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建 -->


**Warnning**

Marboo will init the modified file which file size is zero, which will throw exception. For example, when use "pod install" to install libraries for Xcode project, some file may be inited by Marboo, and the project can not be compiled successfully. More researches will be continued and for now, be careful to use this feature.

# More Help

Also have problems？Contact amoblin ：

| Contact | Me |
|-----|------|
| Email / GTalk | <amoblin@gmail.com> |
| Marboo QQ Group | [273540092](qq://273540092) |
| amoblin's QQ | [576147360](qq://576147360) |
| Weibo | <http://weibo.com/amoblin> |
| Twitter | <http://twitter.com/amoblin> |
| Marboo Homepage | <http://marboo.io> |
