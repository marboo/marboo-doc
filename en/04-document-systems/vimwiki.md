# VimWiki Setup

<!-- create time: 2015-08-06 23:29:42  -->

<!-- This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建 -->

There are 2 steps to setup gitbook support, step 1 is to generate html files, step 2 is to config the path.

A demo will be appear at end.

## Generate HTML

First make sure the build html is generated.

Open index.wiki and run:

```vim
:vimwiki2allhtml<RETURN>
```

then open user config file **marboo_config.json** and find the following content:

```json
"comment": "For GitBook/Sphinx/VimWiki Source Files",
"url_mappings": [{
    "path":"",
    "server": ""
}],
```

add a url mapping as following:

```json
{
    "path": "<VimWiki Path>",
    "server": "VimWiki"
}
```

json key introduction:

- **path** Sphinx Document Source Files Directory, the Marboo Home Directory can be missed.
- **server** Document Type，it's always **VimWiki**

## Demo
