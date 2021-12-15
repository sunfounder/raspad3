Home Assistant文件结构
====================================

Home Assistant默认会在 ``~/.homeassistant`` 路径下创建一个配置文件。

文件目录结构如下：

.. image:: media/image3.png

* ``.storage`` 目录包含了很多与用户相关的信息，包括用户登录信息（用户名/密码，在auth_provider.homeassistant文件中加密）。
* ``configuration.yaml``: 用户编辑的配置文件。
* ``home-assistant.log``: 运行日志（每次重新启动时会清除）。
* ``home-assistant_v2.db``: 数据库
* ``.storage``: 前端配置的各种元素。

