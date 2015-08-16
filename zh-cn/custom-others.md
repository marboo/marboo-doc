# 其他自定义功能
<!-- create time: 2014-12-07 19:00:20  -->

通过修改 **marboo_config.json** 来实现更多的自定义功能。


## 设置对于命令下下创建的文件，是否按照Marboo配置进行内容初始化

```json
    "comment": "设置对于命令下下创建的文件，是否按照Marboo配置进行初始化",
    "init_content_for_commandline": false,
```

默认是false，即不对命令行下创建的文件进行内容初始化。如果改为true，那么在命令行下使用touch创建文件后，Marboo会根据文件类型选择初始化内容。举例如下：

    ➜ $ touch test.md
    ➜ $ cat test.md
    # test
    
    <!-- create time: 2015-07-04 07:27:44  -->
    
    <!-- This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
    本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建 -->

**警告**

从原理上来说，Marboo会对所有文件有修改但大小为0的文件都进行初始化，这在有些情况下会导致问题。比如amoblin用Xcode开发，在用pod install来安装依赖时，就发现有些文件被Marboo初始化了，导致项目编译失败。关于这一块的问题amoblin还在持续研究。目前的话，使用需慎重。
    
# 更多帮助

遇到问题？联系 amoblin ：

| 联系 | 方式 |
|-----|------|
| Email / GTalk | <amoblin@gmail.com> |
| Marboo交流QQ群 | [273540092](qq://273540092) |
| amoblin的QQ | [576147360](qq://576147360) |
| 微博 | <http://weibo.com/amoblin> |
| Twitter | <http://twitter.com/amoblin> |
| Marboo主页 | <http://marboo.io> |
