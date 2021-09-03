Set Boot Up Automatically
=================================

After setting up the self-start, you can open http://localhost:8123 and go directly to Home Assistant. 
The setup steps are as follows.

1. Virtual environment installation.
   
If your Home Assistant is running in a Python virtual environment, please use the following methods:

.. code-block::

    sudo nano -w /etc/systemd/system/home-assistant@homeassistant.service

copy and paste.

.. code-block::

    [Unit]                                                              
    Description=Home Assistant                                        
    After=network-online.target                                          
                                                                        
    [Service]                                                          
    Type=simple                                                         
    User=%i                                                            
    ExecStart=/srv/homeassistant/bin/hass -c "/home/homeassistant/.homeassistant"                                 
                                                                        
    [Install]                                                          
    WantedBy=multi-user.target                                           

Save and exit: Ctrl+ X, Y, Enter.

2. Start self-boot service:

.. code-block::

    # Reload process management                    
                                        
    sudo systemctl --system daemon-reload 

3. Enable service:

.. code-block::

    # Enable Service                                 
                                            
    sudo systemctl enable home-assistant@homeassistant

4. Restart Home Assistant.

.. code-block::

    sudo systemctl restart home-assistant@homeassistant

.. note:: 

    The ``home-assistant@account_name`` in the command, 
    ``account_name`` is set in **Create an account**. 
    If you don't change it, then the default account_name is 
    ``homeassistant``.