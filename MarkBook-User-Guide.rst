=============================
MarkBook用户手册(|version|)
=============================

.. contents:: 目录

.. |date| date:: 2012-12-27
.. title:: 欢迎使用MarkBook
.. author: amoblin <amoblin@gmail.com>
.. publish:: YES
.. |version| replace:: v0.2

欢迎使用MarkBook
=================

欢迎您使用MarkBook，目前版本为 |version|

MarkBook是什么？
================

MarkBook是用来管理置标语言文件的，目前支持reStructuredText和Markdown文件，后续会加入Ascii，wiki等的支持。

通过像类似Evernote的界面来管理，组织Markup文件，实时更新显示HTML输出页面。

自动发布博客到Jekyll/Octopress站点。

关于MarkBook的创作理念，可以看我的 `这篇文章`__

__ http://amoblin.github.com/2012/12/25/MarkBook-release.html

使用MarkBook
=============

新建笔记
---------

点窗口左下角”+“来新建一个笔记，新建时需要指定笔记格式，rst or md。

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

删除笔记
---------

点击窗口左下角“-”来删除笔记。

偏好设置
--------

按[ **Command + ,** ]打开偏好设置，选择喜欢的编辑器即可。

for CLI User
-------------

MarkBook的主目录为~/.MarkBook，里面主要有如下内容：

.. code-block:: console

    $ tree ~/.MarkBook
    MarkBook
    ├── build
    │   └── MyNotes
    │       └── Sample
    │           ├── welcome.rst.html
    │           └── welcome.rst.png
    └── source
        └── MyNotes
            └── Sample
                └── welcome.rst

    6 directories, 3 files
    
其中build用来存放编译生成的html文件，source存放源文件。

source目录下有三层，第一层(MyNotes)是笔记本库，一般也是一个git库(MarkBook会忽略.git目录)。

第二层(Sample)是笔记本，存放各种分类的笔记。

第三层(welcome.rst)就是笔记，可以是.markdown或.md或.rst后缀。

凡是符合上述要求的都会被MarkBook识别，后台更新文件后MarkBook界面会自动同步更新。

下面是我的笔记，仅供参考：

.. image:: https://markbook.googlecode.com/files/markbook.png
    :width: 500
    :height: 300
    :target: https://markbook.googlecode.com/files/markbook.png

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

jekyll/Octorpress用户可以把自己的_posts目录软链到上述目录。具体例子可以看我的文章：`使用MarkBook发布博客到Jekyll`__

__ http://amoblin.github.com/2012/12/26/markbook-to-jekyll.html

TODO
====

Git UI
-------

像Xcode一样显示文件状态，同时添加git pull，git push按钮。

markdown版欢迎页
----------------

由于amoblin一直用rst，不熟悉markdown，所以本说明文档是rst格式的，希望有擅长markdown者写一篇markdown版的，不胜感激。
