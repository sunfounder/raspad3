在开机时启动Home Assistant服务
==================================================

正常情况下，Docker默认开机后是自启动的，这也意味着你安装了Home Assistant后，只要启动树莓派就可以使用了。

您可以使用以下命令查看引导列表。 确认 ``docker.service`` 处于 ``enabled`` 的状态下。

.. raw:: html

    <run></run>

.. code-block::

    sudo systemctl list-unit-files | grep enable


想关闭Docker的自启动，可以输入以下命令：

.. raw:: html

    <run></run>

.. code-block::

    sudo systemctl disable docker.service


开启Docker的自启动，则可以输入以下命令：

.. raw:: html

    <run></run>

.. code-block::

    sudo systemctl enable docker.service