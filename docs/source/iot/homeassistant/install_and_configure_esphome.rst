
安装和配置 ESPHome
==============================


.. note::

    如果你想在 Home Assistant 中添加 ESPHome, 那么你可以通过这个章节来安装和配置它。

    如果你不想添加它，可以选择跳过这一节，直接进入下一节 :ref:`登录`.

`ESPHome <https://esphome.io/>`_ 是为您的 ESP8266/ESP32 开发板创建自定义固件的完美解决方案。 

.. image:: media/esphome_logo.png    
   :align: center

以下是对 ESPHome 工作原理的快速介绍：ESPHome 是一种工具，旨在尽可能简化 ESP 板的管理。它读取一个 YAML 配置文件（就像 Home Assistant）然后在你的 ESP 设备上安装一个自定义固件。在 ESPHome 的配置中添加的设备或传感器将自动显示在 Home Assistant 的 UI 中。

**安装**


1. 安装依赖项。

.. raw:: html

    <run></run>

.. code-block::

    sudo pip3 install cryptography==2.8

2. 安装ESPHome前，需要安装Python并通过pip3安装控制台脚本。

.. note::
    
    安装 ESPHome 1.18.0 或更高版本需要 Python 3.7 或更高版本。

.. raw:: html

    <run></run>

.. code-block::

    sudo pip3 install esphome

或者通过Docker镜像安装（此镜像现在可用于AND64、ARM 和 ARM64（AARCH64）架构）；如果您有其他的架构，请通过 pip 安装 ESPHome 或使用 Home Assistant 插件：

.. raw:: html

    <run></run>

.. code-block::

    docker pull esphome/esphome

3. 打开 ESPHome 仪表板。

.. note::
    在 ESPHome 仪表板中操作时，需要保证此命令正常运行。

.. raw:: html

    <run></run>

.. code-block::

    esphome dashboard config/


**配置 ESPHome**

1. 打开浏览器并通过 http://localhost:6052 或 http://X.X.X.X:6052 (这里的 XXXX 需要替换为您的树莓派IP 地址）进入 ESPHome Dashboard 。

2. 创建配置

单击 \"+\" 开始添加配置。

.. image:: media/image44.png    
   :align: center


输入设备连接所需的名称以及 WiFi 和密码，然后单击 **NEXT**。

.. image:: media/image48.png    
   :align: center


选择设备类型（例如 ESP32）。

.. image:: media/image46.png    
   :align: center


点击NEXT添加完之后，您将在 ESPHome 的仪表板中看到它们。

.. note::

   当不是第一次添加设备时，在主页面点击“+”，按照提示输入设备名称、WIFI和密码，选择设备类型。

   .. image:: media/image53.png    
      :align: center

3. 编辑 ``.yaml`` 文件.

单击右下角的 **EDIT** 进入 ``.yaml`` 文件内部，您将看到以下默认组件。

.. image:: media/desphome_yaml0.png
    :align: center

* ``esphome``: 包含您设置的名称、平台和板类型。
* `logger <https://esphome.io/components/logger.html?highlight=logger>`_: logger 组件通过串口和 MQTT 主题自动记录所有日志消息。
* `api <https://esphome.io/components/api.html?highlight=api>`_: ESPHome 原生 API 用于通过高度优化的网络协议直接与客户端通信。目前，只有 ESPHome 工具和 Home Assistant 使用这个原生 API。
* `ota <https://esphome.io/components/ota.html?highlight=ota>`_: 使用 OTA (Over The Air) 更新组件，您可以将固件二进制文件上传到您的节点，而无需使用 USB 电缆进行上传。 
* `wifi <https://esphome.io/components/wifi.html?highlight=wifi>`_: 这个 ESPHome 组件可以帮您设置 WiFi 连接。必须要配置好，否则 ESPHome 将在配置验证阶段遇到错误。
* `captive_portal <https://esphome.io/components/captive_portal.html?highlight=captive_portal>`_: 这个组件是连接到 WiFi 失败时的回退机制。当尝试连接 WiFi 失败 1 分钟之后，ESP 将启动 WiFi 热点（根据配置启动）。

现在开始添加其他组件。 在 `ESPHome 官方网站 <https://esphome.io/>`_ 中还有很多其它的组件, 包括 **传感器组件**, **输出组件**, **光组件** 等， 下面我们以 **光组件** 为例开始添加。

.. image:: media/image52.png    
   :align: center

将以下代码添加到 ``.yaml`` 文件末尾。

.. code-block::

    # Example configuration entry
    light:
      - platform: binary
        name: "Desk Lamp"
        output: light_output

    output:
      - id: light_output
        platform: gpio
        pin: GPIO16

.. image:: media/desphome_yaml.png
    :align: center

4. 将 ``.yaml`` 文件安装到 ESP32 板上。

编辑完成后点击右下角的 **INSTALL** 进行编译安装。有两种方法供您选择：无线和 USB 端口。但是对于第一次安装，您需要使用 USB 将 ESP32 板连接到树莓派，然后选择第二种安装方法。之后的每一次安装便可以直接通过无线方式安装和编译了。

第一次编译下载依赖大约需要10分钟，请耐心等待。

.. image:: media/install_esp32.png
    :width: 600

安装成功后，如果在 ESP32 板的 GPIO16 上连接一个 LED，您将看到 LED 亮起。记好此IP，将ESPHome添加到Home Assistant时需要填写此IP。

    .. image:: media/install_suc.png 

.. note::

    如果点击 **INSTALL** 没有反应，请清除浏览器缓存，重新安装。

    .. raw:: html

        <run></run>

    .. code-block::

        sudo rm -rf ~/.cache/chromium

ESPHome 配置完成后，便可以将其添加到Home Assistant了。