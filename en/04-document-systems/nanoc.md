# nanoc Setup

<!-- create time: 2015-08-07 06:15:39  -->

<!-- This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建 -->

There are 2 steps to setup gitbook support, step 1 is to generate html files, step 2 is to config the path.

A demo will be appear at end.

## Generate HTML

First make sure the build html is generated.

Open Terminal, enter the nanoc document source files directory, run the following command:

```sh
nanoc
```

## Config Path

then open user config file **marboo_config.json** and find the following content:

    "comment": "For GitBook/Sphinx/VimWiki Source Files",
    "url_mappings": [{
        "path":"",
        "server": ""
    }],


add a url mapping as following:

    {
        "path": "<nanoc Source Files Directory>",
        "server": "nanoc"
    }

if it does not work, add **replace_with** to config the build html path:

```json
{
    "path": "<nanoc Document Source Files Directory>",
    "replace_with": "<nanoc Document Build HTML Path>",
    "server": "nanoc"
}
```

json key introduction:

- **path** nanoc Document Source Files Directory, the Marboo Home Directory can be missed.
- **replace_with** nanoc Generated HTML Files Directory, the Marboo Home Directory can be missed.
- **server** Document Type，it's always **nanoc**

## Demo

