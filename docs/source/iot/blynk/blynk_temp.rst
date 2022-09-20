Temperature Recorder
====================

In this project, you can see the current temperature and the temperature change line graph from Blynk.

.. note:: Before starting this project, we recommend that you complete :ref:`bk_start`. The following will give you a clear understanding of Blynk.




**1. Wiring**

.. image:: img/wiring_blynk_temp.png


**2. Create Widget and Datastream**

1. Click on the menu icon in the upper right corner and select edit dashboard.

    .. image:: img/sp220913_180231.png

2. Add a Gauge widget and a Chart widget to the Dashboard.

    .. image:: img/sp220914_175437.png

3. Create a Datastream for the Gauge widget (I used V5). It will be used to display the temperature. Set **DATA TYPE** to ``Double``, **DECIMALS** to ``#. #`` (two valid decimal places).

    .. image:: img/sp220914_182300.png

4. Add the V5 Datastream you just created to the Chart widget.

    .. image:: img/sp220914_183039.png

#. When finished, click Save And Apply at the top right.

    .. image:: img/sp220913_182300.png


**3. Run the Code**

1. Edit the code

.. raw:: html

   <run></run>

.. code-block:: 

    cd /home/pi/blynk-raspberrypi-python
    sudo nano blynk_temp.py

2. Find the line below and past your ``BLYNK_AUTH_TOKEN``.

.. code-block:: python

    BLYNK_AUTH = 'YourAuthToken'

3. Run the code.

.. raw:: html

   <run></run>

.. code-block:: 

    sudo python3 blynk_temp.py

4. Go to Blynk. Now you can view the temperature and temperature change line graph on the Dashboard.

    .. image:: img/sp220915_101137.png


.. #. If you want to use Blynk on mobile devices, please refer to :ref:`blynk_mobile`.
