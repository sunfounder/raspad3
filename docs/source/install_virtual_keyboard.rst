在 RasPad 上安装虚拟键盘
========================================

当您使用RasPad等触控面板时，可以外接键盘来帮助您进行文字输入操作，但最好安装虚拟键盘。

使用以下命令安装所需的软件。

.. raw:: html

    <run></run>

.. code-block:: shell

  sudo apt install onboard -y
  sudo apt install at-spi2-core

为了让虚拟键盘有更好的效果，还需要做进一步的设置。

单击左上角的树莓派图标并选择 **Preferences** -> **Onboard Settings**。

.. image:: img/onboard.png

在 **General** 选项中, 检查以下两项。 当勾选 **Automatically display when editing text** 时, 会提示重启，所有设置完成后即可重启。

.. image:: img/keyboard1.png

在 **Window** 选项中, 选中 **Dock to screen edge**。

.. image:: img/keyboard2.png

在 **Auto-show** 选项中, 再次选中 **Auto-show when editing text**。

.. image:: img/keyboard3.png


接下来的2项是可选的，图中勾选的是我们推荐的，其他的也可以勾选。

在 **Layout** 选项中, 建议使用 **Small**。

.. image:: img/keyboard4.png

在 **Theme** 选项中, 建议使用 **DarkRoom**。

.. image:: img/keyboard5.png

设置完成后，重启 RasPad。每次重启 RasPad，都需要点击 **General Access** -> **Onboard** 来启用虚拟键盘。

.. image:: img/enable_onboard.png

现在您可以使用此键盘来编辑您的文件或代码。

.. image:: img/keyboard6.png