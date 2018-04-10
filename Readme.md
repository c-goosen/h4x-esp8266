# H4X Meetup

## Meetup About Microcontrollers/IOT (ESP8266)

###
Author: Christo Goosen

mail: christo.goosen@owasp.org / christo.goosen@takectrl.co.za / christogoosen@gmail.com

zatech: @crypticg00se

twitter: @owasp_cpt


## ESP 8266 Getting Started

### Buying:
#### South Africa:
ZAR 90 - > ZAR 200

[Mantech](http://www.mantech.co.za/Stock.aspx?Query=esp8266and)

[Netram (CPT Century City)](https://www.netram.co.za/search?controller=search&orderby=position&orderway=desc&search_query=esp8266&submit_search=)

[Communica (JHB/CPT)](http://www.communica.co.za/Catalog/Browse?search=esp%208266)

#### China

$1.5 -> $5

[Aliexpress](https://www.aliexpress.com/wholesale?catId=0&initiative_id=SB_20180410112630&SearchText=esp+8266)

### Setup & Drivers

Good Guide NODEMCU, OR ARDUINO (ESP-12E)
: http://www.instructables.com/id/Get-Started-with-ESP8266-Using-AT-Commands-NodeMCU/

#### Drivers:
These drivers are needed to connect the esp8266 to your computer's USB via serial. 
##### Linux:
https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers
##### MacOSX:
https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers

or for High Sierra:
http://macappstore.org/wch-ch34x-usb-serial-driver/
or http://www.wch.cn/download/CH341SER_MAC_ZIP.html
##### Windows:
https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers

#### Finding the device via USB
Once the drivers are installed (perhaps with a restart), you will be able to find the esp8266 and connect to it via screen, esptool, etc.

##### Windows:
[Win32](https://github.com/nodemcu/nodemcu-flasher/raw/master/Win32/Release/ESP8266Flasher.exe)

[Win64](https://github.com/nodemcu/nodemcu-flasher/raw/master/Win64/Release/ESP8266Flasher.exe)

[Using Putty](http://flower-platform.com/2015/12/16/esp8266-with-at-commands-connect-from-pc-with-putty/)

##### Mac/Linux/Unix:
Most Linux: `
ls /dev/tty.* `

Most likely on MacOSX: `ls /dev/cu.*`


#### ESPTOOL
This great python tool is great for flashing your compiled firmware to the ESP8266 or erasing the flash.

`pip install esptool`

or

`git clone git@github.com:espressif/esptool.git`

`python setup.py install`

For commands see: https://github.com/espressif/esptool

Example: `esptool.py --port /dev/cu.wchusbserial1420 --baud 115200 erase_flash`

#### NodeMCU (LUA-based firmware)
http://www.nodemcu.com/index_en.html

#### Arduino (C++)

1. Download the Arduino IDE & install https://www.arduino.cc/en/Main/Software
2. Follow this guide to install the esp8266 core: https://github.com/esp8266/Arduino

#### Mongoose-OS (C++/Javascript)

https://mongoose-os.com/docs/quickstart/setup.html

Very easy to install, runs a mini OS with a filesystem etc.

You can upload and download files to and from device. Write in either javascript or c++.



### Flashing the esp8266 firmware

`esptool.py --port /dev/cu.wchusbserial1410 --baud 115200 write_flash 0 firmware/micropython/firmware-combined.bin`



