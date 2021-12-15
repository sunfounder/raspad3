安装摄像头
==================================

打开 RasPad 的后盖。将 FFC 电缆连接到摄像头模块的 CSI 接口。小心地将 CSI 接口电缆穿过 RasPad 后盖上的插槽。连接树莓派的CSI接口。然后小心地关闭 RasPad 的后盖。

.. warning::
  
  SD 卡插槽采用卡扣式连接到后盖。在拆卸或更换后盖之前，请先取出 micro-SD 卡，以免损坏 micro-SD 卡和 RasPad 的内部按键板。

.. image:: img/pir3.jpg
  :width: 600
  :align: center

将带有树莓派操作系统镜像的 micro-SD 卡插入插槽，长按电源键启动 RasPad。

.. image:: img/pir5.jpg
  :width: 500
  :align: center

打开 **树莓派配置**。

.. image:: img/raspbian1.png
  :width: 550
  :align: center

在 **Interfaces** 选项中, **Enable** 使用摄像头, 然后单击 **OK**。

.. image:: img/raspbian2.png
  :width: 500
  :align: center


在弹出的提示框中，选择立即重启。

.. image:: img/raspbian3.png
  :width: 400
  :align: center

重启完成后，使用如下命令行查看摄像头是否可用。

如果出现摄像头画面，则表示摄像头安装成功。否则需要拔下FFC电缆线并重新插入。

.. raw:: html

    <run></run>

.. code-block:: shell

    raspivid -o vid.h264

