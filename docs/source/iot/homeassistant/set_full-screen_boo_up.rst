启动时进入Home Assistant页面
================================================

先体验一下全屏自启动界面。请先关闭已经打开的Home Assistant并运行命令：
``chromium-browser --start-fullscreen "http://localhost:8123"``.

如果您想在开机后自动全屏显示Home Assistant界面，请执行以下操作。


1. 进入 ``autostart`` 文件夹。

.. raw:: html

    <run></run>

.. code-block::

    cd /home/pi/.config/autostart/

.. note::

    如果 ``autostart`` 文件夹不存在，则需要创建一个新文件夹。
    
    .. raw:: html

        <run></run>

    .. code-block::

        sudo mkdir -p /home/pi/.config/autostart/

        
2. 创建 ``chrome_start_fullscreen.desktop`` 文件。

.. raw:: html

    <run></run>


.. code-block::

    sudo nano chrome_start_fullscreen.desktop

3. 编辑 ``chrome_start_fullscreen.desktop`` 文件如下。

.. code-block::

    [Desktop Entry]
    Type = Application
    Exec = chromium-browser --start-fullscreen "http://localhost:8123"

保存并退出依次按: ``Ctrl + X``, ``Y``, ``Enter``.

.. note::
   
    如果要取消全屏启动，将.desktop文件内容用 “#” 注释掉并重启树莓派。

    .. raw:: html

        <run></run>

    .. code-block::

        cd /home/pi/.config/autostart/
        sudo nano chrome_start_fullscreen.desktop


4. 退出全屏。

**计算机:**

方法一：按F11。

方法二：将鼠标移动到屏幕上一栏，点击出现的退出按钮。

方法三：右键弹出菜单，选择 “退出全屏”。

**触摸屏:** 

长按空白处弹出菜单，点击屏幕顶部的退出按钮或选择 “退出全屏”。

.. image:: media/image27.png
    :align: center