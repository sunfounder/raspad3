.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

Install Rotating Screen Service
==================================

The Accel SHIM module was inserted into the Raspberry Pi when the RasPad was assembled, and now we write a script to enable the RasPad to automatically rotate the screen.

This script currently supports the following systems.

**Currently supports**

- Raspberry Pi OS
- Twister OS
- Ubuntu Desktop 21.04

**Run the following commands to install it.**

.. raw:: html

    <run></run>

.. code-block::

    git clone https://github.com/raspad-tablet/raspad-auto-rotator
    cd raspad-auto-rotator
    sudo python3 install.py


After installation, you may be prompted to reboot, if so, the auto-rotate function 
will work after restarting RasPad. If there is no prompt to reboot, 
the auto-rotate function will also work.

**Calibration**

After the first installation, some angles may not trigger the auto-rotation function, please try to turn it in the opposite direction for one second and then turn it back again, it will automatically calibrate. Or rotate RasPad slowly 720 degrees on three axes and it will also auto-calibrate.

If it still doesn't work at some angles no matter how you rotate and calibrate it, in that case, try to recalibrate it with the command.

.. raw:: html

    <run></run>

.. code-block::

    raspad-auto-rotator reset


After running the above command, the auto-rotator will restart. Now recalibrate according to the 2 methods mentioned before.