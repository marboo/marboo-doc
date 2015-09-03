# Gollum Setup

<!-- create time: 2015-08-07 06:20:04  -->

<!-- This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/default.md
本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/default.md 创建 -->

There are 2 steps to setup Gollum support, step 1 is to start Gollum server, step 2 is to config the path.

a demo will be appear at end.

## Run Gollum Server

Open Terminal, enter the Gollum document source files directory, run the following command:

```sh
gollum .
```

## Config Path

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
    "path": "<Gollum Document Source Files Directory>",
    "server": "Gollum"
}
```

if it does not work, add **replace_with** to config the build html path:

```json
{
    "path": "<Gollum Document Source Files Directory>",
    "replace_with": "<Gollum Document Build HTML Path>",
    "server": "Gollum"
}
```

json key introduction:

- **path** Gollum Document Source Files Directory, the Marboo Home Directory can be missed.
- **replace_with** Gollum Generated HTML Files Directory, the Marboo Home Directory can be missed.
- **server** Document Type，it's always **Gollum**

## Demo

