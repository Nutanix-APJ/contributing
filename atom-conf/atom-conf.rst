.. _atom_conf:

-------------
Atom的使用
-------------

这部分文档关于如何用Atom生成文档/workshop。需要如下步骤：

#. 从GitHub组织页面使用**git** 命令行克隆模板

#. 打开 Atom 创建文档

#. 本地保存文档

#. 构建文档，你可以看见结果和页面的外观

#. 提交本地变化

#. 把数据推到个人的GitHub站点

#. 使用git pull 请求上传数据到organizational GitHub


克隆模板
+++++++++++++++++++

在你的机器的某个可选位置生成一个目录（项目）directory (project)。下一步取决于你想运行的**git** 命令。最简单的方法是打开一个命令行或终端回话，然后去向文档的位置。下面截图是从**Mac O/S**看到的一个例子.这个文档使用的地址是**Documents/github/test**。

下方截图显示存放模板的位置内容。

.. figure:: images/1.png
  :width: 600px

为了在我们的机器上获得模板，需要使用 **git** 命令来克隆数据到之前创建的目录(Documents/github/test).

步骤如下:

#. 打开命令行/终端

#. cd 到创建目录的位置

#. 运行命令 **git clone https://github.com/nutanixworkshops/workshop-repo-template**

这些命令后（看下面截图）你将在当前目录的子文件夹里获得本地的数据

.. figure:: images/2.png

复制已克隆的 *workshop-repo-template* 到新的目录或重命名。通过复制你始终可得到新文档需要的的模板。


.. note:: 如果发生改变，你可通过反复前两步和运行命令**git pull https://github.com/nutanixworkshops/workshop-repo-template** 来检查最新的发生的改变。
当你创建完工作所在的目录/创建文档并在之中复制了模板文件，复制一个在工作根目录的叫做.gitignore文档。这将会确保没有不必要的文档上传到GitHub服务器。一个例子是.DS_Dstore 或 thumbs.ini. 下载文档 :download:`.gitignore file <../.gitignore>`. 改变下载的 **txt** 文档到 .gitignore 将它放置于项目的根目录。

开始使用Atom
++++++++++++++++

安装后启动Atom. 启动后会显示如下屏幕视图。

.. figure:: images/5.png

你可以关闭面板并选择你将要做的/下次启动的动作。
打开文档，点击文件 -> 打开并导航到index.rst 文档所在的目录. 打开这个文档你会看见一个带有示例文件的面板/标签。

之上做改变以显示你自己的文档。请参考案例 http://docutils.sourceforge.net/docs/user/rst/quickref.html 。或者查询 google.com on ReStructuredTest 参考文档。

保存文档
++++++++++++++++++++

创建文档之后，在你可以在HTML页面进行修改之前，你需要保存文档。保存文档使之后的提交、推送和创建文档成为可能。

保存文档非常简单，只需要在Atom里保存即可，如你在Word或其他工具里一样。点击 **File -> Save**, 或热键保存数据。

(可选) 构建数据
+++++++++++++++++++++++++

构建数据是指通过工具将创建的文档 (.rst file)转换为HTMl页面。构建HTML页面需要在命令行/终端对话运行 **sphinx-build** 。这意味着sphinx 包如前部分内容所述已经安装了。

下面是所需步骤:

#. 打开命令行/终端回话

#. 改到你要创建文档的根目录。这里举例 Documents/test/test (我拷贝了 workshop-repo-template).

.. figure:: images/3.png
  :width: 300px

#. 运行 **sphinx-build** 命令来创建HTML 页面。命令是 **sphinx-build . _build**. 解释如下:

*  **.** 代表当前目录, 查找 rst 文档并依据文件里的链接。

* **_build** 代表输出的HTML页面文件夹。
.. figure:: images/4.png
  :width: 400px

#. 在浏览器测试布局

.. figure:: images/4a.png

可选 .gitignore 文件
++++++++++++++++++++++++

在根目录增加 .gitignore 文件，你可以告诉git不要推送文件和目录到GitHub的容器。
示例文件显示如下:

::

  # Compiled source #
  ###################
  *.com
  *.class
  *.dll
  *.exe
  *.o
  *.so

  # Packages #
  ############
  # it's better to unpack these files and commit the raw source
  # git has its own built in compression methods
  *.7z
  *.dmg
  *.gz
  *.iso
  *.jar
  *.rar
  *.tar
  *.zip

  # Logs and databases #
  ######################
  *.log
  *.sql
  *.sqlite

  # OS generated files #
  ######################
  .DS_Store
  .DS_Store?
  ._*
  .Spotlight-V100
  .Trashes
  ehthumbs.db
  Thumbs.db

  # Build files #
  ###############
  _build
  build

提交数据
+++++++++++++++

当保存后数据看起来合适的话，你需要确定该变化。需要选择 **Packages -> GitHub -> Toggle Git Tab** (或使用热键).

.. figure:: images/4b.png
  :width: 300px

当屏幕打开，左手边Atom屏幕你会找到带数据的彩色线。这些线表示在本地提交（“写”）后执行的内容。这也是本地GitHub需要执行的内容。 

.. figure:: images/4c.png

通过点击Stage All text (右上角), 所有的操作都被提交。现在你可以选择你不需要的部分，通过选中和右击并选择 **Discard Changes**.

.. figure:: images/4d.png
  :width: 400px

如果你想查看改变，可以点击文件。如果所有的变化都ok，提供一个提交信息并点击 **Commit to master** 按钮.

.. figure:: images/4e.png
  :width: 400px

之后git面板下部的状态条会显示 **Push 1**.

.. figure:: images/4f.png
  :width: 400px

现在我们准备好把数据推送到GitHub个人站点. 点击 **Push 1** 按钮上传数据。

.. figure:: images/4g.png
  :width: 400px
