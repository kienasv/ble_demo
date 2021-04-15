Building
=======

1. Copy ble_demo_nrf52840 folder to /nrfConnectSDK/v1.5.0/zephyr/boards/amr/
2. Configure project and run

Testing
=======

After programming the sample to your development kit, you can test it by connecting to another development kit that runs the :ref:`peripheral_hr_coded`.

1. |connect_terminal_specific|
#. Reset the kit.
#. Program the other kit with the :ref:`peripheral_hr_coded` sample.
#. Wait until the Coded advertiser is detected by the Central.
   In the terminal window, check for information similar to the following::

      Filters matched. Address: xx.xx.xx.xx.xx.xx (random) connectable: yes
      Connection pending
      Connected: xx.xx.xx.xx.xx.xx (random), tx_phy 4, rx_phy 4
      The discovery procedure succeeded

#. Observe that the received notifications are output in the terminal window::

      [SUBSCRIBED]
      [NOTIFICATION] Heart Rate 113 bpm
      [NOTIFICATION] Heart Rate 114 bpm
      [NOTIFICATION] Heart Rate 115 bpm

Dependencies
************

This sample uses the following |NCS| libraries:

* :ref:`gatt_dm_readme`
* :ref:`nrf_bt_scan_readme`

In addition, it uses the following Zephyr libraries:

* ``include/zephyr/types.h``
* ``include/errno.h``
* ``include/zephyr.h``
* ``include/sys/printk.h``
* ``include/sys/byteorder.h``
* :ref:`zephyr:kernel_api`:

  * ``include/kernel.h``

* :ref:`zephyr:bluetooth_api`:

* ``include/bluetooth/bluetooth.h``
* ``include/bluetooth/conn.h``
* ``include/bluetooth/gatt.h``
* ``include/bluetooth/uuid.h``
