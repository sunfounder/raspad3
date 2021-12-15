添加带有 ESP32 的 DIY 设备
==================================

您可以将您购买的智能设备添加到Home Assistant中，例如智能音响、智能台灯等。您也可以使用ESP32制作您的DIY设备并添加。

在本节中，您将学习如何添加 DIY 设备。

在开始以下操作之前，您需要完成 :ref:`安装和配置 ESPHome`.

**添加集成**

1. 现在，访问 http://ip:8123 以进入您的 Home Assistant，然后单击左栏中的 **Configuration** 并选择 **Intergrations**。
   
.. image:: media/image12.png
   :align: center

2. 如果 Home Assistant 在您的网络上找到设备，它会显示相应的集成，只需点击即可将其轻松添加。如果您的智能设备尚未被发现，请不要担心，您可以通过右下角的 **+ ADD INTERGATION** 按钮添加它。
   
.. image:: media/sp210917_111709.png
   :align: center

3. 在弹出的窗口中搜索ESPHome并填写Host (IP在 :ref:`安装和配置 ESPHome` 章节的 INSTALL 步骤后有记录), 可以将你的esp-light放置在卧室、厨房或其他区域。

.. image:: media/add_esphome.png
   :align: center

4. 单击完成后，它会在列表中出现。

.. image:: media/add_esphome1.png
   :align: center

**编辑仪表板**

现在需要添加一个 CARD 来控制这个 esp-light。

点击 **Overview** --> **Edit Dashboard** --> **ADD CARD**, 可以根据需要选择对应的CARD，比如这里选择 **Button**，然后选择对应的Entity。


.. image:: media/edit_dashboard.png
   :align: center
   :width: 800

点击 SAVE 后，您将可以使用该按钮来控制 ESP-light（在 ESP32 板中将 LED 连接到 GPIO16，然后就可以用该按钮来控制 LED 了）。

.. image:: media/sp210917_115819.png
   :align: center

参考 `官方 Demo <https://demo.home-assistant.io/#/lovelace/0>`_ 可以找到更多风格的DIY设备。
