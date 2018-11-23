.. _atom_conf:

-------------
Atom的使用
-------------

这部分文档关于如何用Atom生成文档/workshop。需要如下步骤：

#. 从GitHub组织页面使用**git** 命令行克隆模板

#. 打开 Atom 创建文档

#. 本地保存文档

#. 构建文档，你可以看见结果和页面的外观

#. 确认本地变化

#. 把数据推到个人的GitHub站点

#. 使用git pull 请求上传数据到GitHub的组织站点


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

Make the changes so it will show your documentation. To have a quick reference document, use http://docutils.sourceforge.net/docs/user/rst/quickref.html as and example. Otherwise search google.com on ReStructuredTest reference.

保存文档
++++++++++++++++++++

创建文档之后，在你可以在HTML页面进行修改之前，你需要保存文档。保存文档使之后的确认、推送和创建文档成为可能。

保存文档非常简单，只需要在Atom里保存即可，如你在Word或其他工具里一样。点击 **File -> Save**, 或热键保存数据。

(可选) Build the data
+++++++++++++++++++++++++

Building data means that a tool will translate the create document (.rst file) into HTMl pages. To build the HTML pages the command **sphinx-build** will be run from the command line/terminal session. This means the sphinx packages have been installed as mentioned in pre-requirements part of this workshop.

Steps to take to get a build ready:

#. Open the command line/terminal session

#. Change to the root of the directory of the documentation you want to create. In my example Documents/test/test (I have copied the workshop-repo-template).

.. figure:: images/3.png
  :width: 300px

#. Run the **sphinx-build** command to create the HTML pages. The command is **sphinx-build . _build**. A small explenation:

* The **.** stands for the current directory, search for a rst file and follow the links in the file.

* **_build** stands for the output folder of the HTML pages.

.. figure:: images/4.png
  :width: 400px

#. Test the layout in the browser

.. figure:: images/4a.png

Optional .gitignore file
++++++++++++++++++++++++

By adding a .gitignore file in the root of your directory, you can tell git to NOT push the files and directories into the Repository on GitHub.
An example of such a file is shown below:

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

Commit the data
+++++++++++++++

当保存后数据看起来合适的话，你需要确定该变化。需要选择 **Packages -> GitHub -> Toggle Git Tab** (或使用热键).

.. figure:: images/4b.png
  :width: 300px

When the screen opens, on the lefthand side of the Atom screen you will find colorized line(s) with data. These lines are what will be done on the commit ("write") action local. It will also be the actions that will be produced in the location on GitHub.

.. figure:: images/4c.png

By clicking on the Stage All text (top right corner), all actions are to be committed. Now you can select the one you don't want, by selecting them and right-click and select **Discard Changes**.

.. figure:: images/4d.png
  :width: 400px

If you are interested in the changes, click on the file and you will see what will happen. Are all the changes ok, then provide a Commit message and click on the **Commit to master** button.

.. figure:: images/4e.png
  :width: 400px

After this the status bar at the bottom of the git pane should show **Push 1**.

.. figure:: images/4f.png
  :width: 400px

Now we are all set to push the data towards the GitHub personal part. Click on the **Push 1** button to upload the data.

.. figure:: images/4g.png
  :width: 400px
