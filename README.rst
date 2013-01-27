=============================
Marboo用户手册(|version|)
=============================

.. contents:: 目录

.. |date| date:: 2012-12-27
.. title:: 欢迎使用Marboo
.. author: amoblin <amoblin@gmail.com>
.. publish:: NO
.. |version| replace:: v0.4.1

欢迎使用Marboo
=================

自0.4.1版起，MarkBook改名为Marboo，同时更换了全新的界面。看着还可以吧？

欢迎您使用Marboo，目前版本为 |version|

查看新增了什么功能： https://github.com/marboo/marboo-doc/commits/master

也可以在本地执行下面的操作：

.. code-block:: console

    $ cd ~/.marboo/source/MyNotes.localized/marboo-doc
    $ git log -p

Marboo是什么？
================

Marboo是用来管理置标语言文档及其相关资源的，内置支持格式有如下几种：

* reStructuredText
* Markdown
* HTML (use `twitter bootstrap`_)
* CSS
* JavaScript
* PNG, JPG, GIF等图片格式。
* SHELL脚本。
* Pygments支持的程序文件（语法高亮显示）。

通过 `增加笔记格式`_ 可以支持任意一种置标语言，包括但不限于：

* AsciiDoc
* Wiki
* TextTile

此外，还通过管理CSS和图片来实现Theme样式。

.. _`twitter bootstrap`: http://twitter.github.com/bootstrap/
  
通过像类似Sparrow/Reeder/Evernote的三栏式界面来管理组织Markup文件，实时更新显示HTML输出页面。

自动发布Jekyll/Octopress博客到GitHub/FarBox等。

创作理念
=========

* KISS

    KISS: Keep It Small and Simple

    Marboo只负责显示最终效果，其他的功能像编辑，生成HTML等都可以通过配置来调用程序完成，甚至像增加文件夹这样的操作都是调用Finder来实现的。

* 内容和排版分离

  markdown等适合写内容，css适合排版。下面是一个markdown文件

.. code-block:: markdown

    # 一颗开花的树
    ## 席慕容

    如何让你遇见我  
    在我最美丽的时刻 为这  
    我已在佛前 求了五百年  
    求佛让我们结一段尘缘  

    佛于是把我化作一棵树  
    长在你必经的路旁  
    阳光下慎重地开满了花  
    朵朵都是我前世的盼望  

    当你走近 请你细听  
    那颤抖的叶是我等待的热情  
    而当你终于无视地走过  
    在你身后落了一地的  

    朋友啊 那不是花瓣  
    那是我凋零的心  

最终的展示效果如下：

.. image:: /media/images/marboo/marboo-poem.png

关于Marboo的创作理念，还可以看我的 `这篇文章`__

__ http://amoblin.marboo.biz/2012/12/25/MarkBook-release.html

使用Marboo
=============

首先看一下Gallery上的各种创意用法吧：`Marboo Gallery`_

.. _`Marboo Gallery`: http://marboo.biz/gallery/

本地化支持
***********

Marboo目前支持简体中文和英文。

笔记管理
**********

新建笔记
---------

键入 **Control + N** 或点击窗口上方标题栏中的图标 |new| 来新建一个笔记，新建时需要指定笔记类型（自定义类型见 管理代码_ ）。

.. |new| image:: /media/images/marboo/marboo-icon-new.png
    :width: 25
    :height: 25

注意如果稍后要通过jekyll发布的话，输入的笔记名称最好不要有中文。

因为输入的名字会生成文件名，jekyll对中文文件名的支持不太好。

编辑笔记
--------

双击中栏笔记缩略图，会启动关联的外部编辑器(参见 设置默认编辑器_ )来编辑笔记。保存修改后，Marboo会同步更新内容。

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

.. |open| image:: /media/images/marboo/marboo-icon-open.png
    :width: 25
    :height: 25

删除笔记
---------

点击窗口上方标题栏中的图标 |delete| 或者右键调出菜单选择"删除"来删除笔记。

或者键入 **Delete** 来删除笔记。

.. |delete| image:: /media/images/marboo/marboo-icon-delete.png
    :width: 25
    :height: 25

刷新笔记缩略图
---------------

有时中栏缩略图可能显示为空白，或者是旧主题，这时可以右键点击缩略图，选 “刷新”。

增加笔记本
-----------

双击左栏目录，会在Finder中显示该目录，然后创建文件夹即可，注意须遵循 三层目录规范_

自动化操作
------------

从MarBoo 0.4开始，增加了一个按钮 |make| ,点击它会递归向上查找Makefile或Rakefile文件，然后执行。

.. |make| image:: /media/images/marboo/marboo-icon-make.png
    :width: 25
    :height: 25

Marboo偏好设置
******************

设置默认编辑器
---------------

点击 |config| 或 键入[ **Command + ,** ] 来打开偏好设置，选择喜欢的编辑器即可。

.. |config| image:: /media/images/marboo/marboo-icon-preferences.png
    :width: 25
    :height: 25

修改主题
----------

点击 |theme| 来打开关联的css文件，通过修改css内容来控制所有笔记的外观。

.. |theme| image:: /media/images/marboo/marboo-icon-theme.png
    :width: 25
    :height: 25

添加图片
---------

写MarkDown或RST的同学是不是觉得载入图片的语法太麻烦了？使用Marboo，一切就这么简单：

#. 点击 |import-images| 来选择添加图片
#. 在编辑器中粘贴系统剪切板内容

.. |import-images| image:: /media/images/marboo/marboo-icon-import-images.png
    :width: 25
    :height: 25

也可以这样：

#. 双击左栏media文件夹下的bg-images或images目录，复制文件进去
#. 在中栏找到图片，右键选择"复制该文件路径"
#. 粘贴到css或markdown文件中即可

Evernote相关
****************

导入Evernote笔记
------------------

支持将Evernote笔记导出的HTML导入Marboo。

#. Evernote菜单中选择 文件->导出所有笔记，保存格式为HTML
#. File -> Import Notes...，选中从Evernote中导出的文件夹，点击 open 导入

如果要导入的文件比较多可能需要等待一些时间。

图片画廊展示
**************

Marboo从0.4.1版开始增加了本地图片的画廊展示。Marboo下包含图片文件夹，会生成一个[folder name].gallery.html的文件。

从而将文件夹下的图片在一个WEB页面上展示出来。当然，可以通过css来个性化定制。

Jekyll/Octopress相关
*********************

导入jekyll/Octopress博客
-------------------------

File -> Import Notes...，选择jekyll或Octopress博客的_posts目录，即可将该目录下的博客文章导入到Marboo中。

发布到jekyll/Octopress博客
---------------------------

由于amoblin主要使用rst来写文档，对rst比较熟悉，而md就不太熟悉，所以目前此功能仅支持rst格式。后续会加入md支持。

如果在文件名为my-first-blog.rst的笔记中定义了如下内容：

.. code-block:: rst

    .. |date| date:: 2012-08-31
    .. title:: 博客标题
    .. publish:: YES

就会在 **~/.marboo/source/blogs/my_blog** 目录下创建 2012-08-31-my-first-blog.rst的博客文件，publish为NO时删除上述文件。

本文rst源文件第10行正是定义publish之处，现在值为NO，你可以试着修改为YES，保存，然后点blogs/my_blog看看，是不是出现了？

jekyll/Octorpress用户可以把自己的_posts目录软链到上述目录。

具体例子可以看我的文章：`使用MarkBook发布博客到Jekyll`__

__ http://amoblin.marboo.biz/2012/12/26/markbook-to-jekyll.html

一键发布博客
--------------

把jekyll生成html的命令和git推送的命令都写到Makefile或Rakefile里，放在博客目录下，这样发布博客是不是很方便了呢？

用Marboo发布博客，就这么简单，详情点击 这里_

.. _这里: http://amoblin.puti.biz/2013/01/24/markbook-to-farbox.html

发布到FarBox
-------------

http://amoblin.puti.biz/2013/01/24/markbook-to-farbox.html

读书
******

Pro Git
---------

Git学习的经典著作Pro Git托管在GitHub上，以Creative Commons Attribution-Non Commercial-Share Alike 3.0 license发布。

amoblin整理了Pro Git的源文件，使其符合Marboo的 三层目录规范_ ，发布在GitHub上。

.. code-block:: console

    $ git clone git@github.com:amoblin/progit-for-markbook.git ~/.marboo/source/progit-for-markbook

重启Marboo后，就可以拜读Pro Git了。

写WEB页面
**********

Marboo的 主页_ 就是借助它实现的，有图为证：

.. image:: /media/images/marboo/markbook-self-generate.png
    :height: 600

.. _主页: http://marboo.biz/

管理代码
*********

新建笔记，笔记标题输入程序名，比如hello.py，笔记类型选择最下面的“自定义”，这样生成的文件就不会再添加额外的后缀名了。

粘贴代码进去，保存，Marboo会高亮显示代码。

如果显示内容为：Unknown type of file: [filename]。那么说明Marboo不能识别文件的MIME类型。

这时候可以通过 增加笔记格式_ 来扩展。

Marboo目录组织
=================

Marboo的主目录为~/.Marboo，下面有2个目录：

* build         用来存放生成的HTML文件
* source        源文件

source目录
***********

source目录下3层之内(包括第三层)的目录/文件都会被Marboo管理。

三层目录规范
--------------

source目录下有三层：

第一层(MyNotes.localized)是笔记本库，一般也是一个git库(Marboo会忽略.git目录)。

第二层(marboo-doc)是笔记本，用于存放各种分类的笔记。

第三层(README.rst)是笔记(或图片文件夹)

凡是符合上述要求的文件/目录都会被Marboo识别，source目录下的任何改变都会被Marboo捕获，从而更新用户界面。

典型的3层目录树结构如下：

.. code-block:: console

    source
    └── MyNotes.localized
        └── marboo-doc
            └── README.rst

media目录
-----------

source目录下默认有一个名为media的目录，Marboo的主题样式表、初始化文件模板等存放在这里。

.. code-block:: console

    $ ls media
    bg-images  bin        css        file_types images     templates

* bg-images     背景图片
* bin           生成html的脚本
* css           存放主题样式表
* file_types    存放初始化文件模板
* images        存放笔记文档中的图片
* templates     生成html后外嵌HTML模板

其中 bin/mkldir 是用来创建本地化目录的脚本，上面的MyNotes.localized正是用此创建。(参看 Mac下创建本地化目录_)

build目录
**********

存放source目录生成的HTML等文件，结构上基本和source保持一致，但多出来一个bootstrap目录。

这个bootstrap就是著名的twitter bootstrap，Marboo在引入HTML笔记支持时选择了twitter bootstrap。

.. _Mac下创建本地化目录: http://amoblin.marboo.biz/2013/01/10/create-localized-directory-on-os-x.html

Marboo进阶
=============

Marboo通过CSS来控制笔记的显示效果。

可以配置不同内容的CSS来生成不同的显示版式。相同显示版式的笔记使用相同的二级后缀名，比如

* 我的日记.diary.md     版式为diary的markdown格式笔记
* 志摩的诗.poetry.md    版式为poetry的markdown格式笔记

这样虽然同为markdown文件，使用同一个HTML生成器，但是可以在初始化和最终生成HTML的时候，采取不同的行为。

修改初始化文件内容
*******************

在 新建笔记_ 时，输入笔记名，点击 ‘创建’ 后会生成一个笔记，打开笔记会发现里面已经有内容了，这些内容就是从 media/file_types目录下的文件初始化而来的。

该目录结构如下：

.. code-block:: console

    $ ls file_types
    default.html default.md   default.rst  poetry.md

默认版式的笔记会使用名为default的同格式文件来初始化，而特定版式的笔记会使用对应版式名的同格式文件来初始化。

比如新建一个笔记名为 new.peotry 的MarkDown格式笔记，会使用 poetry.md文件来初始化内容。

通过在此目录添加文件"版式名.格式名"来增加版式。

rst文件初始化
-------------

默认的rst文件初始化内容如下

.. code-block:: rst

    %@
    %@
    %@

    .. Author: your_name
    .. title:: 可以是中文名
    .. |date| date:: %@
    .. publish:: NO

参数用 "%@"表示， 一共4个参数。

* 第2个参数是笔记名
* 第1个和第3个是根据笔记名计算出来的 ‘=’ (RST语法要求)
* 第4个参数是当前日期，主要用于生成jekyll格式的文件名。

md文件初始化
-------------

.. code-block:: markdown

    %@
    %@

* 第1个参数是笔记名
* 第2个是创建时间。

html文件初始化
---------------

这个比较长，不在这里写了，可以打开 media/file_types下的default.html来看。

3个参数：第1个是笔记名(title标签用)，第2个是创建时间，第3个还是笔记名(h1标签用)。

增加笔记格式
***************

对Marboo没有内置的格式，可以在 media/bin 下编写shell脚本来增加支持。

Marboo内置对markdown、rst的支持，但如果该目录下也有对应的HTML生成器，会优先使用该生成器来生成。

比如下面的markdown.sh脚本，在生成的html末尾加上了一行文字：

.. code-block:: console

    #!/bin/sh
    echo "`/usr/local/bin/markdown $1` <br/> generated by markdown.sh"

这样，后缀为markdown的文件，生成的html页面下面都会有这一行文字。

也可以用二级版式来对特定版式的笔记做特定转化。

脚本输入输入接口规范
---------------------

输入：1个参数，为源文件路径
输出：到标准输出，为HTML内容

Marboo通过管道获取脚本的输出来做进一步加工，所以请确保脚本一定要输出内容。

修改笔记HTML模板
*****************

在 media/templates 下保存文件输出模板。

通过标准markdown生成的html文件是只有内容的，并没有html的外部框架，所以通过模板进行包装，从而能够应用css主题。

默认有下面3个模板文件：

* md.html
    \*.md 笔记的输出模板
* poetry.md.html
    \*.peotry.md 笔记的输出模板
* pygmentize.html
    程序文件的输出模板

更新
=====

更新本手册
**********

本文所在目录为一个git仓库，远程仓库地址为：

.. code-block:: console

    $ cd ~/.marboo/source/MyNotes.localized/marboo-doc
    $ git remote -v
    origin	git@github.com:amoblin/marboo-doc.git (fetch)
    origin	git@github.com:amoblin/marboo-doc.git (push)

获取更新：

.. code-block:: console

    $ git pull

更新本软件
***********

菜单项：Marboo -> Check for updates..

或者至 Marboo的下载页_

.. _Marboo的下载页: http://code.google.com/p/markbook/downloads/list

Marboo在发布新版软件前会先更新用户手册，所以如果你想第一时间知道Marboo的动态的话，

可以去 github上的marboo-doc项目_ ，点watch，这样有新的版本发布，你就会收到邮件啦。

.. _github上的marboo-doc项目: https://github.com/marboo/marboo-doc

TODO
====

open folder in terminal
*************************

在终端中打开文件夹，这样可以方便的进行一些操作。

HTML转Markdown
****************

这样导入的Evernote笔记就可以编辑了。

更多的版式
************

谢谢你有耐心看到这里，说明我写的还不是太枯燥啊。Marboo刚接触WEB，不太熟悉。

如果你有漂亮的CSS版式模板，用来实现特定的排版，比如中文竖排，日记，画廊（现在的比较丑）等，同时又愿意给大家分享的话，

请联系 amoblin@gmail.com ，在下一版本里amoblin会添加进来。
