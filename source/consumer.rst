.. _chapter-consumer:

Consumer Edition Reference Platform
===================================

Hardware
--------

[CE 1.0] The hardware that Consumer Reference Platform runs on *should* be
96Boards compliant [ref2]_. The following requirements assume that software runs
on 96Boards CE compliant hardware.

Accelerated graphics support
----------------------------

[CE 2.0] Accelerated graphics drivers *shall* be fully supported either with
open source code, or through royalty free binary drivers. If binary drivers are
utilized, the vendor *shall* provide support to provide updated
drivers/libraries to support new mainline Linux kernel features.

Boot
----

[CE 3.0] It *shall not* be necessary to connect console UART I/O to install an
image into eMMC or microSD, or to startup a pre-installed Debian or AOSP image
on eMMC or microSD card

Kernel
------

Kernel support is required for the following components:

+------------------+---------------------------+
| Component        | Status                    |
+==================+===========================+
| uart             | X                         |
+------------------+---------------------------+
| regulators       | X                         |
+------------------+---------------------------+
| watchdog         | X                         |
+------------------+---------------------------+
| clocks           | X                         |
+------------------+---------------------------+
| runtime PM       | X                         |
+------------------+---------------------------+
| suspend/resume   |                           |
+------------------+---------------------------+
| genpd            |                           |
+------------------+---------------------------+
| cpuidle          | X                         |
+------------------+---------------------------+
| cpufreq          | X                         |
+------------------+---------------------------+
| SATA             | depending on the hardware |
+------------------+---------------------------+
| microSD          | X                         |
+------------------+---------------------------+
| eMMC             | X                         |
+------------------+---------------------------+
| framebuffer      | X                         |
+------------------+---------------------------+
| hdmi             | X                         |
+------------------+---------------------------+
| hdmi audio       | X                         |
+------------------+---------------------------+
| gpu              | X                         |
+------------------+---------------------------+
| spi              | X                         |
+------------------+---------------------------+
| i2c              | X                         |
+------------------+---------------------------+
| gpio             | X                         |
+------------------+---------------------------+
| dsi              | X                         |
+------------------+---------------------------+
| csi              |                           |
+------------------+---------------------------+
| usb otg          | X                         |
+------------------+---------------------------+
| usb host         | X                         |
+------------------+---------------------------+
| usb device       | X                         |
+------------------+---------------------------+
| usb ethernet     | X                         |
+------------------+---------------------------+
| wifi             | X                         |
+------------------+---------------------------+
| bluetooth        | X                         |
+------------------+---------------------------+
| onboard ethernet | depending on the hardware |
+------------------+---------------------------+
| pwm              | X                         |
+------------------+---------------------------+
| pcie             |                           |
+------------------+---------------------------+
| big endian       |                           |
+------------------+---------------------------+
| thermal          | X                         |
+------------------+---------------------------+

Bluetooth
---------

[CE 4.0] Bluetooth *shall* be supported.

The device *shall* be possible to do the following bluetooth actions:

 - Scanning [CE 4.1]
 - Pairing [CE 4.2]
 - Audio Streaming (A2DP) [CE 4.3]
 - File transfer (FTP) [CE 4.4]

List of the reference 3rd party hardware for testing the above mentioned
features will be provided as appendix.

USB
---

The following USB device types *shall* be supported in the software:

 - HID [CE 5.0]
 - Mass storage device [CE 5.1]
 - Ethernet [CE 5.2]

WiFi
----

[CE 6.0] WiFi networking *shall* be supported. The following features *shall*
work:

 - Scanning [CE 6.1]
 - Profiles:

     - Open [CE 6.2]
     - WEP [CE 6.3]
     - WPA2 [CE 6.4]

 - Downloading [CE 6.5]

SD card
-------

[CE 7.0] It *shall* be possible to use SD card for reading and writing data. SD
cards *should* be supported up to SDHC, speed class 10 or UHS class 1.

Power cycle
-----------

The following actions *shall* be possible using software:

 - Shutdown [CE 8.0]
 - Reboot [CE 8.1]

LEDs
----

[CE 9.0] It *shall* be possible to control "user" and "status" LEDs available
on the board from software.

User interface
--------------

[CE 10.0] Graphical user interface (GUI) software builds *shall* be provided.

[CE 10.1] Builds without GUI *may* be provided.

The minimal set of components for GUI:

 - Desktop Environment (for example LXDE)
 - Minimal set of desktop tools

    - Utilities
    - Calculator
    - Image Viewer
    - Text Editor
    - Archive Manager
    - Internet Browser
    - Network Manager
    - System Audio Control
    - Music Player
    - File Manager
    - Process Viewer
    - Terminal

