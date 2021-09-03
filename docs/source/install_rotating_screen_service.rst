Install Rotating Screen Service
==================================

The Accel SHIM module was inserted into the Raspberry Pi when the RasPad was assembled, and now we write a script to enable the RasPad to automatically rotate the screen.

This script currently supports the following systems.

**Compatiable**

Currently supports:

- Raspberry Pi OS
- Twister OS
- Ubuntu Desktop 21.04

**Run the following commands to install it.**


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

.. code-block::

    raspad-auto-rotate reset


After running the above command, the auto-rotator will restart. Now recalibrate according to the 2 methods mentioned before.