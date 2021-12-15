安装旋转屏幕服务
==================================

在组装 RasPad 时将 加速度模块插入到树莓派中，现在我们编写一个脚本使 RasPad 能够自动旋转屏幕。

该脚本目前支持以下系统。

**目前支持**

-树莓派OS
- Twister OS
- Ubuntu Desktop 21.04

**运行以下命令进行安装。**

.. raw:: html

    <run></run>

.. code-block::

    git clone https://github.com/raspad-tablet/raspad-auto-rotator
    cd raspad-auto-rotator
    sudo python3 install.py

安装完成后，可能会提示您重启，如果是这样，重启 RasPad 后自动旋转功能会起作用。如果没有提示重启，自动旋转功能也会起作用。

**校准**

第一次安装后，有些角度可能不会触发自动旋转功能，请尝试反方向转动一秒钟，然后再转动回来，它会自动校准。或者在三个轴上缓慢旋转 RasPad 720 度，它也会自动校准。

如果无论你如何旋转和校准它仍然无法在某些角度工作，在这种情况下，尝试使用命令重新校准它。

.. raw:: html

    <run></run>

.. code-block::

    raspad-auto-rotator reset


运行上述命令后，自动旋转器将重新启动。现在根据前面提到的2种方法重新校准。