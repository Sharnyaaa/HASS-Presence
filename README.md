**Please note I am in the middle of writing out this guide and will fill it out including a link to the enclosure I designed and the code I am using**

This is a guide I am writing on the MMWave sensor I have built for my smart home.

It combines 2 physical sensors as well as a bluetooth proxy for presence detection in rooms of my home.

The Components used for this sensor and links to where I got are from, as long as the physical dimentions of the sensors you use are the same then they will fit in the enclosure, do note its a bit of a tight fit inside though.

**Components Required**

Motherboard - ESP32 (USB C) - https://www.aliexpress.com/p/order/index.html

MMWave Sensor - LD2410b - https://www.aliexpress.com/item/1005005087204432.html

Ambient Light Sensor - BH1750 - https://www.aliexpress.com/p/order/index.html

Enclosure - (Link to printables) 

I designed the above enclosure to suit the components I had selected, with everything inside there isn't a lot of spare room so best to keep wire runs as short as needed for the build, I unsoldered the dupont pins off the ESP board, doing this in future I would recommend getting an ESP32 with no pins on it to save time and space.

First thing I did was Crimp a 5 pin dupont connector to fit the LD2410b

![image](https://github.com/Sharnyaaa/HASS-Presence/assets/73518453/65428451-3863-4a24-bc40-e6b60d7115b5)

The Pinout I am using is below

  VCC (Orange) = 5v
  
  GND (Black) = GND
  
  RX (Turquoise) = P12
  
  Tx (Yellow) = P14

