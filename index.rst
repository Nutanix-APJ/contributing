.. title:: Creating workshops using Atom

.. toctree::
  :maxdepth: 2
  :caption: Pre-requirements
  :name: _pre-reqs
  :hidden:

  Pre-reqs/pre-req

.. toctree::
  :maxdepth: 2
  :caption: Installation
  :name: _install
  :hidden:

  Atom-Installation/atom-inst
  sphinx/sphinx

.. toctree::
  :maxdepth: 2
  :caption: Usage
  :name: _config
  :hidden:

  atom-conf/atom-conf


.. _overview:

-------------------------------
安装 Atom 和 Sphinx
-------------------------------

本文档描述了安装所需工具的方式，以创建名为ReStructredText（RST）的sphinx格式的workshop内容。 使用此方法可以使内容与文档类型“分离”。 首先，我们将使用rst文件作为源，并在互联网上使用sphinx编译器来创建我们在workshop中显示的HTML页面。

.. note:: 要使Atom 集成到 GitHub, 确保你先有一个账号。

安装过程概览
---------------------------------

要获得正确的工具来创建workshop并将其推送到GitHub，将采取以下步骤：

#. 预先需求

#. 下载Atom （这是用于创建.rst文件的示例工具。使用该产品的原因是a）免费且b）可在大多数平台（Mac，Windows和Linux）上使用。 还有其他编辑器工具，但为了易于使用，我们选择了这个产品。

#. 安装Atom

#. 配置Atom

#. (可选) 安装Sphinx. 可选的是Sphinx安装和配置。 在你的计算机上安装Sphinx后，你可以根据离线本地内容生成HTML页面，以查看所有内容是否符合您的预期。

#. 与GitHub集成

#. 从GitHub获得需要的模板

#. 通过模板生成文件

#. 保存创建的文档并运行提交并推送到个人GitHub

#. 将创建的文档拉向Organizational GitHub
