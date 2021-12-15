右键单击 RasPad
===============================

触摸屏平板电脑和显示器使您可以轻松地用手指或手写笔执行简单的导航任务，但在某些时候，您可能希望使用右键单击命令来快速访问特定于上下文的快捷方式。

我们用evdev-rce来使RasPad的右键单击命令仍然可用。

输入以下命令安装所需软件。

.. raw:: html

    <run></run>

.. code-block:: shell

    sudo apt install build-essential libevdev2 libevdev-dev -y
    git clone 'https://github.com/PeterCxy/evdev-right-click-emulation.git'
    cd 'evdev-right-click-emulation'

输入以下命令进行构建。

.. raw:: html

    <run></run>

.. code-block:: shell

  make all

将文件复制到 ``/usr`` 目录中。

.. raw:: html

    <run></run>

.. code-block:: shell

  sudo cp 'out/evdev-rce' '/usr/local/bin/'

使其可执行。

.. raw:: html

    <run></run>

.. code-block:: shell

  sudo chmod +x '/usr/local/bin/evdev-rce'

修改 ``/etc/rc.local`` 使boot-up可用。

.. raw:: html

    <run></run>

.. code-block:: shell

  sudo nano /etc/rc.local

进到 ``rc.local`` 文件之后, 在 ``exit 0`` 前面添加如下命令。

.. code-block:: shell

    sudo /usr/local/bin/evdev-rce &

按 ``Ctrl+C`` -> ``Y`` 退出并保存 ``rc.local`` 文件, 然后运行命令 ``sudo reboot`` 以重新启动 RasPad.

.. raw:: html

    <run></run>

.. code-block:: shell

  sudo reboot

重启后可以长按 RasPad 桌面，看看是否出现右键功能。

.. image:: img/right_click.png
  :align: center