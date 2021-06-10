Appendix
===========

Here, we have included some operations that must be used when doing projects. If you are a new user of RasPad 3, you may need to read this part carefully.

Assemble the Camera Module
--------------------------------------

Open the back cover of the RasPad, connect the FFC cable to the CSI interface of the Camera Module, and pass the RasPad back cover to the CSI interface of the Raspberry Pi.

After that, close up the back cover.

.. warning::
  
  The card slot is set on the back cover and it’s in snap style. Therefore before opening or closing the back cover, you need to take out the microSD card to avoid damaging your microSD card and the internal button board.


.. image:: img/pir3.jpg
  :width: 600
  :align: center

Insert the SD card already burned Raspberry Pi OS into the slot and nd long press the power button to boot the RasPad 3.

.. image:: img/pir5.jpg
  :width: 500
  :align: center

Open **Raspberry Pi Configuration**.

.. image:: img/raspbian1.png
  :width: 550
  :align: center

Then in the Interfaces option above, **Enable** the Camera, and finally click **OK**.

.. image:: img/raspbian2.png
  :width: 500
  :align: center


In the pop-up prompt box, choose to restart now.

.. image:: img/raspbian3.png
  :width: 400
  :align: center

After the restart is complete, use the following command line to check whether the camera is available.

If the camera screen appears, it means that the camera is installed successfully, otherwise the FFC cable needs to be plugged in and unplugged again.

.. code-block:: python

    raspivid -o vid.h264


GPIO Extension Board
------------------------


Before starting the project, you first need to know more about the pins of the Raspberry Pi, which is key to the build circuit.

The pins of Raspberry Pi have three kinds of ways to name and they are wiringPi, BCM and Board. Among these naming methods, 40-pin GPIO Extension board uses the naming method, BCM.

The following table shows us the naming methods of WiringPi, Board and the intrinsic Name of each pin on GPIO Extension board.

For example, for the GPIO17, the Board naming method of it is 11, the wiringPi naming method is 0, and the intrinsic naming method of it is GPIO0. 

.. image:: img/board1.png
  :width: 700
  :align: center

Open the back cover of the RasPad, connect the 40 pin ribbon cable and GPIO extension board, and insert the 40 pin ribbon cable into the Raspberry Pi. After that, cover the back of the RasPad and flip to the front of the RasPad. 

.. warning::
  
  The card slot is set on the back cover and it’s in snap style. Therefore before opening or closing the back cover, you need to take out the microSD card to avoid damaging your microSD card and the internal button board.

.. image:: img/paino2.jpg
  :width: 600
  :align: center

Get the IP Address
------------------------

If You Have a Screen
^^^^^^^^^^^^^^^^^^^^^^^

If you have a screen, it will be easy for you to get the IP address of Raspberry Pi.

+-------------------+--------------------------+ 
| Required Components                          | 
+===================+==========================+ 
| Any Raspberry Pi  | 1 * Power Adapter        | 
+-------------------+--------------------------+ 
| 1 * Micro SD card | 1 * Screen Power Adapter | 
+-------------------+--------------------------+ 
| 1 * HDMI cable    | 1 * Screen               | 
+-------------------+--------------------------+ 
| 1 * Mouse         | 1 * Keyboard             | 
+-------------------+--------------------------+

1. Insert the SD card you’ve set up with Raspberry Pi OS into the micro SD card slot on the underside of your Raspberry Pi.
2. Plug in the Mouse and Keyboard.
3. Connect the screen to Raspberry Pi’s HDMI port and make sure your screen is plugged into a wall socket and switched on.
  .. note::
      If you use a Raspberry Pi 4, you need to connect the screen to the HDMI0  (nearest the power in port).
4. Use the power adapter to power the Raspberry Pi. After a few seconds, the Raspberry Pi OS desktop will be displayed.
5. Place the mouse on the wifi icon, and the IP of the Raspberry Pi will be displayed after a period of time.

.. image:: img/appendix1.png
  :width: 700
  :align: center

If You Have No Screen
^^^^^^^^^^^^^^^^^^^^^^^

After the Raspberry Pi is connected to WIFI, we need to get the IP address of it. There are many ways to know the IP address, and two of them are listed as follows.

**1. Checking via the router**
   
If you have permission to log in the router(such as a home network), you can check the addresses assigned to Raspberry Pi on the admin interface of router. 

The default hostname of the Raspberry Pi OS is raspberrypi, and you need to find it. (If you are using ArchLinuxARM system, please find alarmpi.)

**2. Network Segment Scanning**
   
You can also use network scanning to look up the IP address of Raspberry Pi. You can apply the software, **Advanced IP scanner** and so on.

Scan the IP range set, and the name of all connected devices will be displayed. Similarly, the default hostname of the Raspberry Pi OS is raspberrypi, if you haven't modified it.

Use the SSH Remote Control
------------------------------

We can open the Bash Shell of Raspberry Pi by applying SSH. Bash is the standard default shell of Linux. The Shell itself is a program written in C that is the bridge linking the customers and Unix/Linux. Moreover, it can help to complete most of the work needed. 

**For Linux or/Mac OS X Users**

Go to **Applications** -> **Utilities**, find the **Terminal**, and open it. 

.. image:: img/appendix3.png
  :width: 600
  :align: center

Type in **ssh pi@ip_address** . “pi”is your username and “ip_address” is your IP address. For example:

.. code-block:: python

    ssh pi@192.168.18.197 

Input”yes”.

.. image:: img/appendix4.png
  :width: 600
  :align: center

Input the passcode and the default password is **raspberry**.

.. image:: img/appendix5.png
  :width: 600
  :align: center

We now get the Raspberry Pi connected and are ready to go to the next step.

.. image:: img/appendix6.png
  :width: 600
  :align: center

.. note::
    When you input the password, the characters do not display on window accordingly, which is normal. What you need is to input the correct password.

**For Windows Users**

If you're a Windows user, you can use SSH with the application of some software. Here, we recommend PuTTY.

Download PuTTY, open it and click Session on the left tree-alike structure. Enter the IP address of the RPi in the text box under Host Name (or IP address) and 22 under Port (by default it is 22).

.. image:: img/appendix7.png
  :width: 600
  :align: center

Click **Open**. Note that when you first log in to the Raspberry Pi with the IP address, there prompts a security reminder. Just click **Yes**. 

When the PuTTY window prompts “**login as:**”, type in “**pi**”(the user name of the RPi), and **password**: “raspberry” (the default one, if you haven't changed it). 

.. image:: img/appendix8.png
  :width: 600
  :align: center

Here, we get the Raspberry Pi connected and it is time to conduct the next steps.

.. note::
  When you input the password, the characters do not display on window accordingly, which is normal. What you need is to input the correct password.






