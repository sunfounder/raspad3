Start the Home Assistant Service at Boot
==================================================

Normally, Docker is self-starting after booting by default, which also means that after you install Home Assistant, you can use it as long as you start the Raspberry Pi.

You can use the following command to view the boot list. The ``docker.service`` should be in the ``enabled`` state.

.. raw:: html

    <run></run>

.. code-block::

    sudo systemctl list-unit-files | grep enable


To turn off Docker's self-startup, please enter the following command:

.. raw:: html

    <run></run>

.. code-block::

    sudo systemctl disable docker.service


To enable Docker's self-startup, please enter the following command:

.. raw:: html

    <run></run>

.. code-block::

    sudo systemctl enable docker.service