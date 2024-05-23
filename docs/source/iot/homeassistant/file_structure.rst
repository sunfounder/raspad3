.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

Home Assistant File Structure
====================================

Homeassistant creates a configuration file by default under the path of the executing user 
(created homeassistant) at the ``~/.homeassistant`` path.

The file directory structure is as follows:

.. image:: media/image3.png

* ``.storage`` directory contains a lot of user-related information, including user login information (username/password, encrypted in auth_provider.homeassistant file).
* ``configuration.yaml``: User-edited configuration files.
* ``home-assistant.log``: Run log (cleared with each reboot).
* ``home-assistant_v2.db``: Database..
* ``.storage``: Various elements of front-end configuration.

