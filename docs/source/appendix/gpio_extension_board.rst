GPIO 扩展板
=========================


在开始项目之前，您首先需要更多地了解树莓派的引脚，这是搭建电路的关键。

树莓派的引脚有三种命名方式。它们是wiringPi、BCM 和Board。40 针 GPIO 扩展板使用 BCM 命名方式。

下表显示了三种命名方式以及 GPIO 扩展板上每个引脚的固有名称。

例如GPIO17，其Board命名方式为11，wiringPi命名方式为0，其固有命名方式为GPIO0。

.. image:: img/board1.png
  :width: 700
  :align: center

打开 RasPad 的后盖，将 40 针带状电缆线插入树莓派。将带状电缆线穿过 RasPad 底座上的可用插槽，并将 40 针带状电缆线的另一端连接到 GPIO 扩展板。然后更换 RasPad 的后盖。

.. warning::
  
  SD 卡插槽采用卡扣式连接到后盖。在拆卸或更换后盖之前，请先取出 micro-SD 卡，以免损坏 micro-SD 卡和 RasPad 的内部按键板。
  
.. image:: img/paino2.jpg
  :width: 600
  :align: center