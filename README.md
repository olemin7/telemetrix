# platformio
source ~/.platformio/penv/bin/activate
pio run
pio project init --ide eclipse
# Telemetrix4Esp8266
https://github.com/MrYsLab/Telemetrix4Esp8266
# Board
http://arduino.esp8266.com/stable/package_esp8266com_index.json
# lib 
https://github.com/olemin7/esp_libs

# referenses
schematic: https://circuits.io/circuits/3798057-net-clock-led
gtest
https://www.codeproject.com/Articles/811934/Cplusplus-unit-test-start-guide-how-to-set-up-Goog
https://github.com/google/googletest.git
arduino:
https://github.com/arduino/Arduino/blob/master/build/shared/manpage.adoc

# esp8266 reference
http://www.kloppenborg.net/blog/microcontrollers/2016/08/02/getting-started-with-the-esp8266

##wemos
Pin |mcuPin | Function    | ESP-8266 Pin | used
TX  |  1    | TXD         | TXD          |
RX  |  3    | RXD         | RXD          |
A0  |       | ADC, 3.3V   | A0           | battery
D0  |  16   | IO          | GPIO16       |
D1  |  5    | IO, SCL     | GPIO5        | 
D2  |  4    | IO, SDA     | GPIO4        | 
D3  |  0    | IO, 10k P-up| GPIO0        | 
D4  |  2    | IO, 10k P-up,LED|   GPIO2  | DHT.data
D5  |  14   | IO, SCK     | GPIO14       | 
D6  |  12   | IO, MISO    | GPIO12       | 
D7  |  13   | IO, MOSI    | GPIO13       | 
D8  |  15   | IO, 10k P-down, SS|  GPIO15|
G   |       | Ground      | GND          |
5V  |       | 5V          | -            |
3V3 |       | 3.3V        | 3.3V         |
RST |       | Reset       | RST          |


#ADC wemos
 A0--
    |
   220K
    |--- ADC
   100K
    |
   GND
 
#battery
 vbat 130k --A0
 adc val= 848,volt=3.72656 (3.95

#DHT
1 vcc (3.3V)
2 data (D4)
3 nc
4 GND (G)

#deepsleep
D0->RST Connect GPIO16 to RST pin only after uploading the code

[scratch]

https://mryslab.github.io/s3-extend/s3-extend/
source .venv/bin/activate
python -m venv .venv

pip3 install s3-extend
s3e