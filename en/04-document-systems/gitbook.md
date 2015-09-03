# GitBook Setup

<!-- create time: 2015-08-03 07:34:57  -->

<!-- This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建 -->

There are 2 steps to setup gitbook support, step 1 is to generate html files, step 2 is to config the path.

A demo will be appear at end.

## Generate HTML

First make sure the build html is generated.

Open Terminal, enter the gitbook document source files directory, run the following command:

```sh
gitbook build
```

## Config Path

Open user config file **marboo_config.json** and find the following content:

```json
"comment": "For GitBook/Sphinx/VimWiki doc Source Files",
"url_mappings": [{
    "path":"",
    "server": ""
}],
```

add a url mapping as following：

```json
{
    "path": "<GitBook Document Source Files Directory>",
    "server": "GitBook"
}
```

if it does not work, add **replace_with** to config the build html path:

```json
{
    "path": "<GitBook Document Source Files Directory>",
    "replace_with": "<GitBook Document Build HTML Path>",
    "server": "GitBook"
}
```

json key introduction:

- **path** GitBook Document Source Files Directory, the Marboo Home Directory can be missed.
- **replace_with** GitBook Generated HTML Files Directory, the Marboo Home Directory can be missed.
- **server** Document Type，it's always **GitBook**

## Demo

this is the gitbook config for Marboo User Guide:

```json
{
    "path": "/Guide.localized/en_US.localized",
    "server": "GitBook"
}
```

also you can config the html path:

```json
{
    "path": "/Guide.localized/en_US.localized",
    "replace_with": "/Guide.localized/en_US.localized/_book",
    "server": "GitBook"
}
```
