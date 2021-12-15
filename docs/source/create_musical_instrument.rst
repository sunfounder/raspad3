制作乐器
===================================

描述
-------------

您可以将 RasPad 3 变成与朋友一起玩的游戏屏幕、显示天气和时间的智能闹钟、监控机器人动作的显示器以及许多其他功能。

本文将向您展示如何使用您的 RasPad 3 DIY 乐器。让我们一起来看看吧！

.. image:: img/paino1.jpg
  :width: 600
  :align: center

所需组件
-------------------------------

- A RasPad 3
- 8G+ SD Card
- Scratch 3 (either online or offline)
- Micro SD卡读卡器
- 40pin排线
- T型拓展板
- 面包板
- 按键
- 10k电阻
- 一些跳线

你会学到
---------------------

- 在 Scratch 上使用笔记功能。
- 从 GPIO 引脚输入按钮值。
  
课程指南
--------------

搭建电路
^^^^^^^^^^^^^^^^^^^^^^

首先连接GPIO扩展板，具体步骤请阅读 :ref:`GPIO 扩展板`。

.. image:: img/pir2.jpg
  :width: 600
  :align: center

将T型GPIO扩展板插入面包板，搭建电路如下图。

.. image:: img/paino3.png
  :width: 600
  :align: center

用 Scratch 3 编程
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

将SD卡插入RasPad 3的插槽，然后长按电源键启动RasPad 3。

.. image:: img/install_sd_card.jpg
  :width: 500
  :align: center

.. warning::
  
  卡槽位于后盖，采用卡扣式。 因此在打开或关闭后盖之前，您需要取出 microSD 卡，以免损坏您的 microSD 卡和内部按键板。

Scratch 3 主页的左侧是一些排列整齐的代码块，您可以拖动它们来编程。 在这个项目中，我们需要添加另外两个功能：音乐和树莓派GPIO。 演奏乐器和鼓的音乐功能，以及树莓派GPIO 功能可用于控制树莓派的整个引脚。

.. image:: img/paino5.jpg
  :width: 600
  :align: center

点击左下角的添加图标，选择音乐和树莓派GPIO，在Scratch 3主页面左侧添加两个功能。

.. image:: img/paino6.jpg
  :width: 700
  :align: center

结束程序

.. image:: img/paino7.jpg
  :width: 700
  :align: center

按下面包板上的这三个按钮，就会发出“哆、来、咪”的声音。

.. image:: img/paino8.jpg
  :width: 600
  :align: center

如果你不喜欢看文字，下面可以观看视频

.. raw:: html

  <iframe width="695" height="576" src="https://www.youtube.com/embed/Ku4vRZz-x2I" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

在本文中，我们将介绍如何使用 RasPad 3 创建乐器。 当然，你可以发挥你所有的想象力和灵感来升级你的乐器，例如你可以添加更多的按钮、音符和 LED 来制作一个很酷的八音盒。