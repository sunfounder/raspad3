.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

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