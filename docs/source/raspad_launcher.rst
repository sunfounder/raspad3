RASPAD LAUNCHER
==================


Introduction
------------------
RasPad Launcher is an open source software that simulates a launcher menu, with a focus on improving the users touchscreen experience with the RasPad or other touchscreens.

.. image:: img/raspad-launcher.jpg

.. note::
    If you want to use the original desktop of the Raspberry Pi, you can skip this chapter.

Why we abandon RasPad OS and launch RasPad Launcher
--------------------------------------------------------
RasPad OS intergrated with RasPad Launcher, RasPad FAQ with our custom UI and boot animations, which is redundant. And people loves the idea of RasPad Launcher, so we decided to remove all unnecessary components, and keep RasPad Launcher as a single application. So people can install it your own Raspberry Pi OS.

Installation Guide
--------------------

Download the RasPad Launcher package, and extract it.

.. code-block::

    wget https://github.com/raspad-tablet/raspad-launcher/releases/download/v1.4/raspad-launcher.zip
    unzip raspad-launcher.zip
    cd raspad-launcher


The script will install the following:

* Qt runtime.
* RasPad launcher with desktop profile.
* RasPad FAQ desktop profile (Just a quick icon to browser RasPad FAQ webpage).
* display auto rotate for Accl SHIM.

Run install script.

.. code-block::

    chmod +x install
    sudo ./install

.. note::

    To manually install RasPad Launcher and specific components, please refer to `RasPad Launcher <https://github.com/raspad-tablet/raspad-launcher/blob/main/docs/installation-guide.md>`_.