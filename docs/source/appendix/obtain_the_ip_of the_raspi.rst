.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

Obtain the IP Address of the Raspberry Pi
================================================

With a Screen
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

1. Insert the micro-SD card with the Raspberry Pi OS image into the micro SD card slot on the underside of the Raspberry Pi.
2. Plug in the Mouse and Keyboard.
3. Connect the screen to the Raspberry Pi’s HDMI port. Make sure the screen is plugged into a wall socket and turned on.

  .. note::

    For the Raspberry Pi 4 models, connect the screen to the HDMI0 port, nearest to the power-in socket.

4. Use the power adapter to power the Raspberry Pi. After a few seconds, the Raspberry Pi OS desktop will be displayed.
5. Hover the cursor over the WiFi icon, and the IP address of the Raspberry Pi will be displayed.

.. image:: img/appendix1.png
  :width: 700
  :align: center

Without a Screen
^^^^^^^^^^^^^^^^^^^^^^^

After the Raspberry Pi is connected to WIFI, we need to get the IP address of it. There are many ways to know the IP address, and two of them are listed as follows.

**1. Checking via the router**

Check the addresses assigned to Raspberry Pi on the administration interface of the router.

The default hostname of the Raspberry Pi OS is raspberrypi. If you are using an ArchLinuxARM system, please find alarmpi.

**2. Network Segment Scanning**
   
Network scanning applications can be used to look up the IP address of Raspberry Pi, such as Advanced IP Scanner.

Scan the IP range set, and the names of all connected devices will be displayed. The default hostname of the Raspberry Pi OS is raspberrypi.
