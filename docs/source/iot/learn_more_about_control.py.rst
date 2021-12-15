详细了解 control.py
================================

为了更好的理解后面的项目，我们先来看看 Cloud4RPi 官方提供的示例代码。

.. note::

    在查看本章之前，请先完成上一章 :ref:`Cloud4RPi的快速使用指南` 。

打开 ``control.py`` 文件。

.. raw:: html

    <run></run>

.. code-block:: shell

    cd cloud4rpi-raspberrypi-python
    sudo nano control.py

Cloud4RPi 会为每个设备设置一个设备令牌，您需要用正确的设备令牌填写变量 DEVICE_TOKEN 才能连接到相应的设备。

.. code-block:: python

    DEVICE_TOKEN = '556UfPaRw6r6rDKYfzx5Nd1jd'

``variables`` 是一个二维字典，它的每个键对应的值也是一个字典。

``variables`` 字典的键包括 ``'Room Temp'``, ``'LED On'``, ``'CPU Temp'``, ``'STATUS'``, ``'Location'``, 它们都是显示在控制面板小部件上的数据。
    
``variables`` 字典中每个键的值也是一个字典，这些字典的键是一样的，其中 ``'bind'`` 键的值是一个可以返回传递内容的函数，是传递内容 ``'type'`` 的数据类型（ ``'numeric'`` 是数字类型， ``'string'`` 是字符串类型， ``'bool'`` 是布尔类型， ``'location'`` 是包含两个字典的列表）。

通过对 ``variables`` 字典的分析，我们可以知道 Cloud4RPi 会读取 ``variables`` 字典的键值，并在控制面板中显示键值对应的值。显然我们不能改变 ``variables`` 字典的键，但是我们可以改变键中的值（ ``'bind'`` 字典的值），让 widgets 显示我们想要的内容。

比如我们要向 Cloud4RPi 发送湿度值，虽然不能在 ``variables`` 字典中添加一个新的键 ，但是可以借用其中的键，比如 ``'Room Temp'``，然后在其 ``'bind'`` 的值里面编写返回湿度值的函数。

.. code-block:: python

    variables = {
        'Room Temp': {
            'type': 'numeric' if ds_sensors else 'string',
            'bind': ds_sensors[0] if ds_sensors else sensor_not_connected
        },
        'LED On': {
            'type': 'bool',
            'value': False,
            'bind': led_control
        },
        'CPU Temp': {
            'type': 'numeric',
            'bind': rpi.cpu_temp
        },
        'STATUS': {
            'type': 'string',
            'bind': listen_for_events
        },
        'Location': {
            'type': 'location',
            'bind': get_location
        }

``vdiagnostics`` 中存储有关树莓派的信息，并用于验证，防止错接。

.. code-block:: python

    vdiagnostics = {
        'CPU Temp': rpi.cpu_temp,
        'IP Address': rpi.ip_address,
        'Host': rpi.host_name,
        'Operating System': rpi.os_name,
        'Client Version:': cloud4rpi.__version__,
    }
