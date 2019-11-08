### About
This is an example of PWM based on 40MHz SSI stream (1-bit serial) for RTL8710, RTL8711 and RTL8195.


### Prerequisites
You will need a RTL8710 module, an ARM Cortex-M compatible SWD debugger.

RTL8710 modules are easy to find on eBay or Aliexpress, the B&T BT-00 variant
is hard to miss. Pine64 is about to release their own version of this module,
called PADI: https://www.pine64.org/?page_id=946

If you are looking for a development board with integrated SWD debugger, I can
recommend the Ameba RTL8710 Board http://www.amebaiot.com/en/ameba-sdk-boards/
Those can be bought for around $20 on Aliexpress.

You will also need a copy of the GCC based SDK for this chip. It can be
downloaded from Pine64's PADI web site. Look under Resources and download
the "Ameba RTL8710AF SDK ver v3.5a GCC ver 1.0.0- without NDA"

After extracting the SDK, follow the instructions found in
"doc/UM0096 Realtek Ameba-1 build environment setup - gcc.pdf" to prepare
the SDK. If you are using OpenOCD, you should also change the JTAG clock speed
from 10kHz to 1MHz in component/soc/realtek/8195a/misc/gcc_utility/openocd/ameba1.cfg

Make sure you can build and upload the standard SDK firmware. If everything
works, make a "clean_all" and clone this repository into the project folder.
This project can be built in the same way as the standard project, just use
the folder rtl8710_40MHz_PWM_SSI/GCC-RELEASE as base folder.


### Misc
More information about and support for the RTL8710 can be found on the following forums:
PADI IoT Stamp Forum: http://forum.pine64.org/forumdisplay.php?fid=57
and
RTL8710 Community Forum: https://www.rtl8710forum.com/
