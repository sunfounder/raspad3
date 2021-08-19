Right Click on RasPad
===============================

Touchscreen tablets and displays make it easy for you to perform simple navigation tasks with your fingers or stylus, but at some point, you may want to use right-click commands to quickly access context-specific shortcuts.

Here we use ``evdev-rce`` to make RasPad's right-click command still available.

Enter the following command to install the required software.

  .. code-block:: shell

    sudo apt install build-essential libevdev2 libevdev-dev
    git clone 'https://github.com/PeterCxy/evdev-right-click-emulation.git'
    cd 'evdev-right-click-emulation'

Enter the following command to build.

  .. code-block:: shell

    make all

Copy the file to the ``/usr`` directory.

  .. code-block:: shell

    sudo cp 'out/evdev-rce' '/usr/local/bin/'

Make it executable.

  .. code-block:: shell

    sudo chmod +x '/usr/local/bin/evdev-rce'

Modify the ``/etc/rc.local`` file to enable boot-up.

  .. code-block:: shell

    sudo nano /etc/rc.local

After entering ``rc.local``, add the following command before ``exit 0``.

  .. code-block:: shell

    sudo /usr/local/bin/evdev-rce &

Press ``Ctrl+C`` -> ``Y`` to exit and save the ``rc.local`` file, and then run ``sudo reboot`` to restart RasPad.

.. code-block:: shell

  sudo reboot

After restarting, you can long press on the RasPad desktop and see if the right click function appears.

.. image:: img/right_click.png
  :align: center