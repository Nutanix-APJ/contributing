.. _installsphinx:

--------------
安装 Sphinx
--------------

为什么在本地安装Sphinx?
+++++++++++++++++++++++++

检查你为Sphinx创建的文档，并上传到nutanixworkshop.com，你可以安装Sphinx编译器。

安装
++++++++++++

.. note:: 本文档假定已安装了Python预制包。如果没有，请使用: https://docs.python-guide.org/starting/installation/

1. 打开一个命令行

2. 使用pip 安装命令安装需要的sphinx和依赖工具

运行下面的命令 (https://www.sphinx-doc.org/en/master/usage/installation.html#installation-from-pypi):

* pip install sphinx

* pip install sphinxcontrib-fulltoc

* pip install sphinx-bootstrap-theme

* pip install sphinx_fontawesome


这个安装结束后，你可以使用sphixn制定的命令生成创建页面的HTML版本。想了解Sphinx是做什么的，请参看: https://youtu.be/oJsUvBQyHBs. 鉴于你已经“拷贝”了模板，就不必运行``sphinx-quickstart`` 命令了。你可以直接运行带参数的``sphinx-build`` 。
