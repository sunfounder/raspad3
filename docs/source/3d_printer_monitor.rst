3D Printer Monitor
==========================

When using a 3D printer, we will need to use OctoPrint. It is an open source 3D printer controller application, which provides a web interface for the connected printers. It displays printers' status and key parameters and allows user to schedule prints and remotely control the printer.

Please refer to the detailed installation tutorial of OctoPrint: https://community.octoprint.org/t/setting-up-octoprint-on-a-raspberry-pi-running-raspbian-or-raspberry-pi-os/2337.

This tutorial has written very detailed installation steps, which may take a long time and requires more patience.

.. note::

    * Before starting the tutorial, you will need to install Raspberry Pi OS on your MicroSD card, please refer to :ref:`Install OS to Your Micro SD Card`.
    * In step-**Optional: Webcam**, you will need to install a camera on RasPad 3. For the camera installation tutorial, please refer to :ref:`Assemble the Camera Module`.
    * In step-**Optional: Touch UI** may be wrong, please refer the following content to configure the **Touch UI** function.

Touch UI
-----------

When using the **Touch UI** function, if you cannot find the ``autostart`` file in the ``~/.config/lxsession/LXDE-pi`` path, you may need to add the file manually (new image generally encounter this situation).

First create the ``lxsession`` folder and the ``LXDE-pi`` folder.

.. code-block:: python

    mkdir ~/.config/lxsession
    mkdir ~/.config/lxsession/LXDE-pi

Copy the ``autostart`` from the path ``/etc/xdg/lxsession/LXDE-pi``.

.. code-block:: python

    cp /etc/xdg/lxsession/LXDE-pi/autostart ~/.config/lxsession/LXDE-pi/autostart

Set the permissions of the ``autostart`` file to be readable and writable, and then open it.

.. code-block:: python   

    chmod 644 ~/.config/lxsession/LXDE-pi/autostart
    nano .config/lxsession/LXDE-pi/autostart

Add the following line at the end of the ``autostart`` file to make RasPad3 execute the ``startTouchUI.sh`` script file every time before booting.

.. code-block:: python

    @/home/pi/startTouchUI.sh

After restarting RasPad3, you will see the full screen of OctoPrint's Touch UI. You can also press ``F11`` to exit the full screen.

Make a 3D Model
------------------

Click this link: `https://projects.raspberrypi.org/en/projects?hardware%5B%5D=3d-printer <https://projects.raspberrypi.org/en/projects?hardware%5B%5D=3d-printer>`_, refer to the official Raspberry Pi tutorial, you can get the 3D model file in the format of .stl.

Generally, 3D printers cannot directly process .stl files. You need to use Ultimaker Cura software to slice them, and then upload them to the 3D printer through OctoPrint to print the 3D model file.

Download Ultimaker Cura from https://ultimaker.com/software/ultimaker-cura，choose **Download for free**.

.. image:: img/oct2.png
  :width: 600
  :align: center

Select the version you need. Since Ultimaker Cura is not available on the Raspberry Pi system, you need to perform the slicing operation on your computer.

.. image:: img/oct3.png
  :align: center

When installing Ultimaker Cura, please note that in the **choose components** step, **Open STL files with Cura** has been checked by default, so that .stl files can be sliced.

If you want to slice other types of model files, check the corresponding option, otherwise you can install it directly.

.. image:: img/oct4.png
  :width: 600
  :align: center

When opening Ultimaker Cura for the first time, you need to understand and configure it.

Special attention is that in the **Add a printer** step, you need to select the correct printer model and click Next.

.. image:: img/oct5.png
  :width: 600
  :align: center

After selecting the printer model, check whether the parameters provided by Ultimaker Cura are correct.

If there is an error, modify it directly. Finally, follow the instructions to complete the configuration of Ultimaker Cura.

.. image:: img/oct6.png
  :width: 600
  :align: center

Click the open icon in the upper left corner, and then add the .stl 3D model file that needs to be sliced.

.. image:: img/oct7.png
  :width: 600
  :align: center

After the addition is complete, click the **Slice** option in the lower right corner, and Ultimaker Cura will automatically perform the slicing operation.

.. image:: img/oct8.png
  :width: 400
  :align: center

After slicing is complete, click the **Save to Disk** option in the lower right corner to save the sliced ​​file locally.

.. image:: img/oct9.png
  :width: 400
  :align: center

Select the file type recognized by your printer, and then click **Save**.

.. image:: img/oct10.png
  :width: 600
  :align: center


Print 3D Model
--------------------

After slicing the .stl file, we can send the sliced ​​3D model file to your 3D printer through OctoPrint, and then it can be printed.

Enter ``http://192.168.18.179/?#temp>`` in your browser to log in to OctoPrint.

.. note::

  Before logging into OctoPrint's web UI, you should have successfully installed OctoPrint on RasPad 3.

  Replace the IP address 192.168.18.179 to yours. Place the mouse on the wifi icon, and the IP of the Raspberry Pi will be displayed after a period of time.

  .. image:: img/appendix1.png
    :width: 700
    :align: center

Now you have entered OctoPrint.

.. image:: img/oct11.png
  :width: 700
  :align: center

Click the **Upload** option to select the sliced ​​3D model file.

.. image:: img/oct12.png
  :width: 600
  :align: center

Click the **print** icon. The 3D printer starts to print the 3D model file after the slicing process.

.. image:: img/oct13.png
  :width: 500
  :align: center

If you have transferred the sliced ​​file to the Raspberry Pi, you can also open the OctoPrint UI in RasPad to print.

.. image:: img/oct14.png
  :width: 700
  :align: center


Video
-------

The following video shows that after installing OctoPrint, connect your 3D printer and RasPad 3 through a USB cable，upload the designed 3D file, and then use the camera to monitor the printing process. 

You can also monitor the temperature to prevent the temperature from getting too low or too high, which will affect the model.

.. raw:: html

    <iframe width="695" height="576" src="https://www.youtube.com/embed/ml3-Su6Yenc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>





