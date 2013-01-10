=============================
MarkBook用户手册(|version|)
=============================

.. contents:: 目录

.. |date| date:: 2012-12-27
.. title:: 欢迎使用MarkBook
.. author: amoblin <amoblin@gmail.com>
.. publish:: NO
.. |version| replace:: v0.2.3

欢迎使用MarkBook
=================

欢迎您使用MarkBook，目前版本为 |version|

MarkBook是什么？
================

MarkBook是用来管理置标语言文件的，目前支持的格式有下面几种：

笔记格式
---------

* reStructuredText
* Markdown
* HTML5 (use `twitter bootstrap`_)

.. _`twitter bootstrap`: http://twitter.github.com/bootstrap/
  
后续会加入Ascii，Wiki等的支持。

通过像类似Sparrow/Reeder/Evernote的三栏式界面来管理组织Markup文件，实时更新显示HTML输出页面。

自动发布博客到Jekyll/Octopress站点。

关于MarkBook的创作理念，可以看我的 `这篇文章`__

__ http://amoblin.github.com/2012/12/25/MarkBook-release.html

使用MarkBook
=============

新建笔记
---------

键入 **Control + N** 或点击窗口上方标题栏中的图标 |new| 来新建一个笔记，新建时需要指定 笔记格式_

.. |new| image:: ../../../images/new.png

注意如果稍后要通过jekyll发布的话，输入的笔记名称最好不要有中文。

因为输入的名字会生成文件名，jekyll对中文文件名的支持不是很好。

编辑笔记
--------

双击中栏笔记缩略图，会启动关联的外部编辑器(参见 偏好设置_)来编辑笔记。保存修改后，MarkBook会同步更新内容。

下面是c代码样例：

.. code-block:: c

    #include <stdio.h>

    int main() {
        char* a[3];
        int i;
        a[0] = "你好";
        a[1] = "hello";
        a[2] = "world!";

        printf("a's address is: %p\n", a);
        for(i=0; i<3; i++) {
            printf("%p: %s\n", a[i], a[i]);
        }
    }

预览笔记
---------

右栏实时更新生成的HTML页面，若要同时浏览多个页面，点击 |open| 来用默认浏览器打开当前页面。

.. |open| image:: ../../../images/open.png

删除笔记
---------

点击窗口上方标题栏中的图标 |delete| 来删除笔记。

或者键入 **Delete** 来删除笔记。

.. |delete| image:: ../../../images/delete.png

偏好设置
--------

点击 |config| 或 键入[ **Command + ,** ] 来打开偏好设置，选择喜欢的编辑器即可。

.. |config| image:: ../../../images/config.png

导入jekyll/Octopress博客
-------------------------

File -> Import Notes...，选择jekyll或Octopress博客的_posts目录，即可将该目录下的博客文章导入到MarkBook中。

导入的操作是复制了一份，所以对导入的博客的修改不影响导入源。

发布到jekyll/Octopress博客
---------------------------

由于amoblin主要使用rst来写文档，对rst比较熟悉，而md就不太熟悉，所以目前此功能仅支持rst格式。后续会加入md支持。

如果在文件名为my-first-blog.rst的笔记中定义了如下内容：

.. code-block:: rst

    .. |date| date:: 2012-08-31
    .. title:: 博客标题
    .. publish:: YES

就会在 **~/.MarkBook/source/blogs/my_blog** 目录下创建 2012-08-31-my-first-blog.rst的博客文件，publish为NO时删除上述文件。

本文第10行正式定义publish之处，现在值为NO，你可以试着修改为YES，保存，重启MarkBook，看看有什么？

jekyll/Octorpress用户可以把自己的_posts目录软链到上述目录。具体例子可以看我的文章：`使用MarkBook发布博客到Jekyll`__

__ http://amoblin.github.com/2012/12/26/markbook-to-jekyll.html

for CLI User
-------------

MarkBook的主目录为~/.MarkBook，里面主要有如下内容：

.. code-block:: console

    .MarkBook
    ├── bin
    │   └── mkldir
    ├── bootstrap
    │   ├── css
    │   │   ├── bootstrap-responsive.css
    │   │   ├── bootstrap-responsive.min.css
    │   │   ├── bootstrap.css
    │   │   └── bootstrap.min.css
    │   ├── img
    │   │   ├── glyphicons-halflings-white.png
    │   │   └── glyphicons-halflings.png
    │   └── js
    │       ├── bootstrap.js
    │       └── bootstrap.min.js
    ├── build
    │   └── MyNotes.localized
    │       └── markbook-doc
    │           ├── README.rst.html
    │           └── README.rst.png
    ├── images
    │   ├── config.png
    │   ├── delete.png
    │   ├── new.png
    │   └── open.png
    ├── source
    │   └── MyNotes.localized
    │       └── markbook-doc
    │           └── README.rst
    └── style
        ├── Reeder-Noise.png
        └── default.css

    13 directories, 18 files

各文件/目录作用如下：

* bin   常用命令
* bin/mkldir 创建本地化目录(参看 博文_)
* bootstrap twitter-bootstrap
* build 存放编译生成的HTML文件
* images 存放文档中需要显示的图片
* source    存放源文档 **切记保存好**
* source/MyNotes.localized  本地化目录：我的笔记
* source/blogs/my_blog   publish为YES时生成Jekyll风格文件至此
* style                  rst2html.py中style-template的参数

.. _博文: http://amoblin.github.com

三层目录规范
-------------

source目录下有三层，第一层(MyNotes)是笔记本库，一般也是一个git库(MarkBook会忽略.git目录)。

第二层(Sample)是笔记本，存放各种分类的笔记。

第三层(MarkBook-User-Guide.rst)就是笔记，可以是.markdown或.md或.rst后缀。

凡是符合上述要求的都会被MarkBook识别，后台更新文件后MarkBook界面会自动同步更新。

下面是我的笔记，仅供参考：

.. image:: https://markbook.googlecode.com/files/markbook.png
    :width: 500
    :height: 300
    :target: https://markbook.googlecode.com/files/markbook.png

Pro Git
---------

Git学习的经典著作Pro Git托管在GitHub上，以Creative Commons Attribution-Non Commercial-Share Alike 3.0 license发布。

amoblin整理了Pro Git的源文件，使其符合MarkBook的 三层目录规范_ ，发布在GitHub上。

.. code-block:: console

    $ git clone git@github.com:amoblin/progit-for-markbook.git ~/.MarkBook/source/progit-for-markbook

重启MarkBook后，就可以拜读Pro Git了。

更新本手册
----------

本文所在目录为一个git仓库，远程仓库地址为：

.. code-block:: console

    $ cd ~/.MarkBook/source/MyNotes.localized/markbook-doc
    $ git remote -v
    origin	git@github.com:amoblin/markbook-doc.git (fetch)
    origin	git@github.com:amoblin/markbook-doc.git (push)

获取更新：

.. code-block:: console

    $ git pull

更新本软件
-----------

菜单项：MarkBook -> Check for updates..

或者至 MarkBook的下载页_

.. _MarkBook的下载页: http://code.google.com/p/markbook/downloads/list

TODO
====

multi markup support
----------------------

通过插件形式支持更多的置标语言。

Git UI
-------

像Xcode一样显示文件状态，同时添加git pull，git push按钮。

markdown版欢迎页
----------------

由于amoblin一直用rst，不熟悉markdown，所以本说明文档是rst格式的，希望有擅长markdown者写一篇markdown版的，不胜感激。
