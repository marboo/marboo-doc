# 其他自定义功能
<!-- create time: 2014-12-07 19:00:20  -->

通过修改用户配置文件(详见[5.1 配置文件介绍](./config-file.html))来实现更多的自定义功能：

## 设置中栏显示的文件类型

默认为空数组，表示显示全部文件

```json
    "only_show_files": []
```

若只需要显示Markdown文件，配置如下：

```json
    "only_show_files": ["*.md", "*.mdk", "*.markdown"]
```

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

## 设置生成的HTML文件是否保留原文件扩展名

默认为false，不保留原文件扩展名。这时文件 test.md 生成的HTML文件为 test.html。如果同一个文件夹下有多个不同扩展名的文件，那么在切换文件时可能需要手动刷新。

```json
    "generate_html_with_file_extension": false
```

也可以设置为保留扩展名。这时文件 test.md 生成的HTML文件为 test.md.html，不会和其他文件生成的HTML文件重复了。

## 忽略指定的文件夹，不显示在Marboo左栏

默认不显示在左栏的文件夹如下：

```json
"ignored_dirs": ["Pods", "_book", "xcuserdata", ".git"],
```

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
