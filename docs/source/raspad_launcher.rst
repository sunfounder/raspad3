RasPad Launcher
==================


Introduction
------------------
RasPad Launcher is an open source software, simulating a launcher menu, focus on improving touch experience with RasPad, or other touchscreen.

.. image:: img/raspad-launcher.jpg

.. note::
    If you want to use the original desktop of the Raspberry Pi, you can skip this chapter.

Why we abandon RasPad OS and launch RasPad Launcher
--------------------------------------------------------
RasPad OS intergrated with RasPad Launcher, RasPad FAQ with our custom UI and boot animations, which is redundant. And people loves the idea of RasPad Launcher, so we decided to remove all unnecessary components, and keep RasPad Launcher as a single app. So people can install it your own Raspberry Pi OS.

Installation Guide
--------------------

**Download Package**

Download RasPad Launcher package, and extract it.

.. code-block::

    wget https://github.com/raspad-tablet/raspad-launcher/releases/download/v1.4/raspad-launcher.zip
    unzip raspad-launcher.zip
    cd raspad-launcher

**Quick install with a script**

If you don't really know what's going on, and don't care about messing up your own settings, like a brand new Debian. Or you are lazy enough to manual install everything, you can use the quick install script. The script will install these things:

* Qt runtime
* RasPad launcher with desktop profile
* RasPad FAQ desktop profile (Just a quick icon to browser RasPad FAQ webpage)
* display auto rotate for Accl SHIM
* Run install script

.. code-block::

    chmod +x install
    sudo ./install

.. note::
    If you want to manually install RasPad Launcher and learn more about it, please refer to `RasPad Launcher <https://github.com/raspad-tablet/raspad-launcher/blob/main/docs/installation-guide.md>`_.