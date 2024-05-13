This is a guide I am writing on the MMWave sensor I have built for my smart home.

It combines 2 physical sensors as well as a bluetooth proxy for presence detection in rooms of my home.

The Components used for this sensor and links to where I got are from, as long as the physical dimentions of the sensors you use are the same then they will fit in the enclosure, do note its a bit of a tight fit inside though.

**Components Required**

Motherboard - ESP32 (USB C) - https://www.aliexpress.com/p/order/index.html

MMWave Sensor - LD2410b - https://www.aliexpress.com/item/1005005087204432.html

Ambient Light Sensor - BH1750 - https://www.aliexpress.com/p/order/index.html

Enclosure - [(Link to printables) ](https://www.printables.com/model/876849-presense-sensor-enclosure)

I designed the above enclosure to suit the components I had selected, with everything inside there isn't a lot of spare room so best to keep wire runs as short as needed for the build, I unsoldered the dupont pins off the ESP board, doing this in future I would recommend getting an ESP32 with no pins on it to save time and space.

First thing I did was Crimp a 5 pin dupont connector to fit the LD2410b

![image](https://github.com/Sharnyaaa/HASS-Presence/assets/73518453/65428451-3863-4a24-bc40-e6b60d7115b5)

The Pinout I am using is below

  VCC (Orange) = 5v
  
  GND (Black) = GND
  
  RX (Turquoise) = P12
  
  Tx (Yellow) = P14

I soldered the other ends of the leads into the related pads on the ESP then took the cable from the BH1750 and trimmed the wires to size and soldered those to the board with the below pinout

  VCC (Red) = 3v3
  
  SCL (Brown) = P22
  
  Data (White) = P21

  Ground (Black) = Ground

  This is what it looked like once I had both sensors wired up to bench test
![Immich photo 1332](https://github.com/Sharnyaaa/HASS-Presence/assets/73518453/8ce9a5c5-0660-4280-a665-e49168ab6617)

Then put it all in the case and tested a final time before using hot glue to secure the ESP board in place then attaching the lid, its friction fit and stays closed just fine

![Immich photo 1339](https://github.com/Sharnyaaa/HASS-Presence/assets/73518453/6d6a04c6-a431-4229-b0e8-0ce8d10ce60a)

![Immich Photo 1336](https://github.com/Sharnyaaa/HASS-Presence/assets/73518453/bf32d65b-1434-481a-a5e9-57011bd0a11c)

Finally using the YAML in the file in this repo in ESPhome the sensor should show up and be ready to tune and use
