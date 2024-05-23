.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

Add Smart Devices
=================================

You can add your purchased smart devices to Home Assistant, such as smart sound, smart desk lamp, etc. You can also make your DIY device with ESP32 and add it in.

In this section, you will learn how to add your smart devices.

**1. Configure the Smart Device**

You need to make sure that your smart device has been assigned an IP. 
You can complete this step through the corresponding APP of the smart device. 
For example, the picture below shows a bedside lamp configured with **HomeKit**.

.. image:: media/pair_device.png
   :align: center
   :width: 800


**2. Add Integration**

Now, visit http://ip:8123 to access your Home Assistant, then click Configuration in the left column and select Intergrations.


.. image:: media/image12.png
   :align: center

If Home Assistant finds a device on your network, it will display the corresponding integration, which can be easily added with just a few clicks. 

.. image:: media/sp210917_111709.png
   :align: center

If your smart device has not been discovered yet, don’t worry, click the **+ ADD INTEGRATION** button at the bottom right and search for your integration in the list.

.. image:: media/image19.png
    :align: center


Each integration may be different in use, you can visit `Home Assistant Integration <https://www.home-assistant.io/integrations/>`_ for details.

**Edit Dashboard**

Now a CARD needs to be added to control this smart device.

Return to the Overview page. If the device you just added does not appear, you need to **Edit Dashboard**.

Click **Overview** –> **Edit Dashboard** –> **ADD CARD**, you can select the corresponding CARD according to your needs, for example, select Button here, and then select the corresponding Entity.

.. image:: media/edit_dashboard.png
   :align: center
   :width: 800

After adding the corresponding card, click **Done** to exit editing, and then you can control your smart device.

.. image:: media/sp210917_115819.png
   :align: center
