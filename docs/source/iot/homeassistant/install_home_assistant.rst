Install Home Assistant
================================

**Install Docker**

Here will introduce how to use the container environment to install and run Home Assistant. 
We recommend using Docker as the container environment. 
The way to install Docker is very simple, just run the following commands.

.. raw:: html

    <run></run>

.. code-block::

    curl -fsSL https://get.docker.com -o get-docker.sh
    sudo sh get-docker.sh

.. note:: 
    
    You can see more details in `Install Docker Engine on Debian <https://docs.docker.com/engine/install/debian/#install-using-the-convenience-script>`_.


**Install Home Assistant**

After installing the container environment, if you are using **Raspberry Pi 3**, run the following commands to install the Home Assistant.

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

If you are using **Raspberry Pi 4**, run the following commands to install the Home Assistant.

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

    For more details, please see `Install Home Assistant Container <https://www.home-assistant.io/installation/raspberrypi>`_.

**Start the Home Assistant Service**

After the installation is complete, you can run the following command to start Home Assistant.

.. raw:: html

    <run></run>


.. code-block::

    sudo docker start homeassistant

Use the following command to close Home Assistant.

.. raw:: html

    <run></run>


.. code-block::

    sudo docker stop homeassistant

Restart Home Assistant with the following command.

.. raw:: html

    <run></run>

.. code-block::

    sudo docker restart homeassistant

**Enter Home Assistant Page**

Now you can enter ``http://<localhost>:8123`` in the browser to enter the Home Assistant operation interface. For example, my Raspberry Pi IP is 192.168.6.136, then visit ``http ://192.168.6.136:8123``.

.. note::
    
    1. If you need to configure boot-up, please refer to: :ref:`Start the Home Assistant Service at Boot`
    
    2. If you need to configure a full screen boot, please refer to: :ref:`Enter the Home Assisant Page at Boot`

