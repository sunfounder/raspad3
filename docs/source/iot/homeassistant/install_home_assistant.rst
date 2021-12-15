安装Home Assistant
================================

**安装 Docker**

这里将介绍如何使用容器环境来安装和运行 Home Assistant。我们推荐使用 Docker 作为容器环境。安装 Docker 的方法很简单，运行如下命令即可。

.. raw:: html

    <run></run>

.. code-block::

    curl -fsSL https://get.docker.com -o get-docker.sh
    sudo sh get-docker.sh

.. note:: 
    
    你可以在这里查看更多信息 `如何安装Docker <https://docs.docker.com/engine/install/debian/#install-using-the-convenience-script>`_.


**安装Home Assistant**

安装容器环境后，如果你使用的是 **树莓派3**, 运行以下命令安装Home Assistant。


.. raw:: html

    <run></run>


.. code-block::

    sudo docker run -d \
    --name homeassistant \
    --privileged \
    --restart=unless-stopped \
    -e TZ=MY_TIME_ZONE \
    -v /home/pi/homeassistant:/config \
    --network=host \
    ghcr.io/home-assistant/raspberrypi3-homeassistant:stable

如果您使用的是 **树莓派4**, 则请运行以下命令来安装Home Assistant。

.. raw:: html

    <run></run>


.. code-block::

    sudo docker run -d \
    --name homeassistant \
    --privileged \
    --restart=unless-stopped \
    -e TZ=MY_TIME_ZONE \
    -v /home/pi/homeassistant:/config \
    --network=host \
    ghcr.io/home-assistant/raspberrypi4-homeassistant:stable

.. note:: 

    更多详细信息, 请查阅 `安装 Home Assistant 容器 <https://www.home-assistant.io/installation/raspberrypi>`_.

**启动Home Assistant服务**

安装完成后，您可以运行以下命令启动Home Assistant。

.. raw:: html

    <run></run>


.. code-block::

    sudo docker start homeassistant

使用以下命令关闭Home Assistant。

.. raw:: html

    <run></run>

.. code-block::

    sudo docker stop homeassistant

使用以下命令重新启动Home Assistant。

.. raw:: html

    <run></run>

.. code-block::

    sudo docker restart homeassistant

**进入Home Assistant页面**

现在你可以在浏览器中输入 ``http://<localhost>:8123`` 来进入 Home Assistant 操作页面. 例如我的树莓派IP是 192.168.6.136, 然后便可以访问 ``http ://192.168.6.136:8123``.

.. note::
    
    1. 如果需要配置开机启动, 请参考: :ref:`在开机时启动Home Assistant服务`
    
    2. 如果需要配置开机进入Home Assistant页面, 请参考: :ref:`启动时进入Home Assistant页面`

