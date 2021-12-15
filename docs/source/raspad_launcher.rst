RASPAD Launcher
==================

介绍
------------------
RasPad Launcher 是一款模拟启动器菜单的开源软件，专注于改善用户使用 RasPad 或其他触摸屏的触摸屏体验。

.. image:: img/raspad-launcher.jpg

.. note::
    如果你想使用树莓派的原始桌面，你可以跳过这一章。

安装指南
--------------------

下载 RasPad Launcher 安装包并解压

.. raw:: html

    <run></run>

.. code-block::

    wget https://github.com/raspad-tablet/raspad-launcher/releases/latest/download/raspad-launcher.zip
    unzip raspad-launcher.zip
    cd raspad-launcher

该脚本将安装以下内容

* 带有桌面配置文件的 RasPad Launcher。
* RasPad 常见问题桌面配置文件（只是浏览器 RasPad 常见问题网页的快速图标）。
* 显示Accl SHIM的自动旋转。

运行安装脚本。

.. raw:: html

    <run></run>

.. code-block::

    chmod +x install
    sudo ./install

.. note::

    要手动安装 RasPad Launcher 和特定组件，请参阅 `RasPad Launcher <https://github.com/raspad-tablet/raspad-launcher/blob/main/docs/installation-guide.md>`_.