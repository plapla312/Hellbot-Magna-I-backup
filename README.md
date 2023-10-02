# Hellbot-Magna-I-backup
How to backup the flash and eeprom of a mega2560  https://forum.arduino.cc/t/how-to-backup-the-flash-and-eeprom-of-a-mega2560/886107/2

En mi Windows 7 con una placa Geetech GT2560 v3.0 (clon?) fue:

cd C:\Users\Pau\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/bin/

Leer flash:
avrdude "-CC:\Users\Pau\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/etc/avrdude.conf" -v -V -patmega2560 -cwiring "-PCOM21" -b115200 -D "-Uflash:r:backup_flash.hex:i"

Leer eeprom:
avrdude "-CC:\Users\Pau\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/etc/avrdude.conf" -v -V -patmega2560 -cwiring "-PCOM21" -b115200 -D "-Ueeprom:r:backup_eeprom.hex:i"
