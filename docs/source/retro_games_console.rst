Retro Games Console
======================

Description
-------------

You can turn RasPad 3 into a retro games console playing with your friends, let's see how we can do it!

.. image:: img/retropie1.jpg
  :width: 500
  :align: center

Required Components
-------------------------------

- A RasPad 3
- 8G+ MicroSD Card
- MicroSD Card Reader
- Keyboard
- Gamepad

Any version of Raspberry Pi is OK for you, but for an easier and smoother experience of playing games, we suggest you use Raspberry Pi 4 as the main control board. With the nearly one-year R&D, the Retro Pie is now compatible with Raspberry Pi 4.

That Raspberry Pi uploads or downloads the game system and game ROM needs taking up a large memory, so we suggest you to use SD card with big memory to avoid the failure of configuration out of lacking storage. 

.. image:: img/retropie2.jpg
  :width: 350
  :align: center

When playing games, a gamepad and a keyboard are needed.

.. image:: img/retropie3.jpg
  :width: 500
  :align: center

RasPad 3, the best choice of game consoles, is a multifunctional tablet computer whose main control board is Raspberry Pi. Equipped with a 1280*800 high resolution LCD touch screen, a 2W stereo speaker, 3 USB3.0 ports, RasPad3 features high picture and sound quality, smooth running, thus giving you excellent game experience.

.. image:: img/retropie4.jpg
  :width: 600
  :align: center


Game System Installation
---------------------------------

We select RetroPie as our game system. RetroPie allows you to turn your Raspberry Pi, ODroid C1/C2, or PC into a retro-gaming machine. It builds upon Raspbian OS, Emulation Station, RetroArch and many other projects to enable you to play your favorite Arcade, home-console, and classic PC games with the minimum set-up.

.. image:: img/retropie5.png
  :width: 500
  :align: center

At first, download the SD image compatible with the Raspberry Pi 4 on the `RetroPie <https://retropie.org.uk/>`_ official website .

.. image:: img/retropie6.png
  :width: 700
  :align: center

After the download, unzip the package downloaded and you will see the image file inside.

Then flash the RetroPie image into the your MicroSD card.

* For Windows: `Raspberry Pi Imager <https://www.raspberrypi.org/software/>`_, `Etcher <https://www.balena.io/etcher/>`_, or `Win32DiskImager <https://sourceforge.net/projects/win32diskimager/>`_.

.. note::

  Win32DiskImager requires an .img file extracted from the .img.gz image downloaded in step #2. You can use a program like 7zip to do this.

* For macOS: `Raspberry Pi Imager <https://www.raspberrypi.org/software/>`_, `Etcher <https://www.balena.io/etcher/>`_, `Apple Pi Baker <https://www.tweaking4all.com/software/macosx-software/macosx-apple-pi-baker/>`_, or the dd command.
* For Linux: `Raspberry Pi Imager <https://www.raspberrypi.org/software/>`_, `Etcher <https://www.balena.io/etcher/>`_, or the dd command

.. note::
  MacOS/Linux users can optionally extract the .img image from the downloaded .img.gz by using gunzip (macOS users can also simply double-click it).

.. image:: img/retropie8.png
  :width: 600
  :align: center

Next, Insert the SD card into the RasPad 3 and then press the power button to booting RasPad 3.

.. warning::
  
  The card slot is set on the back cover and it’s in snap style. Therefore before opening or closing the back cover, you need to take out the microSD card to avoid damaging your microSD card and the internal button board.



Configurations
----------------------

After booting RasPad 3, you should do the following steps, such as Controller Configuration, Configure WiFi and Transferring ROMs. A keyboard and a gamepad are needed when do these steps.

The detailed steps are shown in the video:

.. raw:: html

    <iframe width="695" height="576" src="https://www.youtube.com/embed/qIZcwXvhl8Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

.. note::
    1. You can also go to RetroPie official website to detailed tutorial: `RetroPie Docs <https://retropie.org.uk/docs/First-Installation/>`_.
    2. RetroPie allows you to turn your Raspberry Pi or PC into a retro-gaming machine. But because of the nature/complexity of copyright/intellectual property law (country-specific), RetroPie doesn't provide ROMs for games. If you want to get them, you can download from the forum or Google to find the sources, then place one ROM under the directory of ``RetroPie emluator``.

Here, we find the ROM of **Super Mario 3**. If you have fought the ROMs of other games, you can download them and then you can play the games by RasPad 3. That’s very easy. 

.. image:: img/retropie10.jpg
  :width: 600
  :align: center
