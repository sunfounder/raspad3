Calibrate the Rotating Screen Function
================================================

.. note::
  
  The rotating screen feature is only available for the Raspberry Pi OS.

Every time after you install the Raspberry Pi OS, you need to recalibrate the built-in Accel SHIM module so that the rotating screen function can work properly.

The calibration steps are as follows：

First run the calibration script.

.. code-block:: shell

  git clone https://github.com/raspad-tablet/raspad-auto-rotator
  cd raspad-auto-rotator
  sudo python3 install.py

Wait for the installation process to complete, and restart RasPad according to the prompts.

After the RasPad restarts, it will automatically enter the calibration procedure. At this time, follow the steps below to rotate the RasPad 3.

Rotate 360° from left to right, and finally return to the front.

.. image:: img/rotate1.jpg

Then rotate 360° from top to bottom, and finally return to the front.

.. image:: img/rotate2.jpg
  :width: 400

Place the RasPad flat on the desktop and rotate it 360 degrees.

.. image:: img/rotate3.jpg
  :width: 600

After the calibration is complete, press ``Ctrl + C`` to exit the calibration script.

.. code-block:: shell

  sudo reboot