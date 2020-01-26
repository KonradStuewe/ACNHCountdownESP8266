# ACNHCountdownESP8266

This is a little countdown for Animal Crossing New Horizon I made.
It runs on an ESP8266 (Wemos D1 mini) and uses a TCA9548A I2C multiplexer to talk to the OLED displays.

![Screens off](/img/Screens_off.jpg)
![Screens on](/img/Screens_on.jpg)

### Disclaimer

I haven't originally planed to publish this, so there are no comments and the code could use a bit of a cleanup.
I plan to that in the future but till then you'll have to live with this. :)

## Parts

* ESP8266
   * I used a Wemos D1 mini but any ESP8266 development board should be fine.
   * In theory most other boards should work too as long as they support I2C and have a way of connecting to the internet to acquire  the time. A Real-Time-Clock module would also work but that would need further modifications to the current code.
*  TCA9548A I2C Multiplexer
   * I got mine from [*here*](https://www.aliexpress.com/item/32888007073.html?spm=a2g0s.9042311.0.0.27424c4dohvo00)
* I2C OLED Displays
   * Basically any I2C display that is supported by the [u8g2 library](https://github.com/olikraus/u8g2)
   * I used [these](https://www.aliexpress.com/item/32844104782.html?spm=a2g0s.9042311.0.0.27424c4dohvo00) (1.3 inch 4pin) for the bigger displays and [these](https://www.aliexpress.com/item/32637598943.html?spm=a2g0s.9042311.0.0.27424c4dohvo00) (black pcb) for the smaller ones
   * Most other displays should work fine too, but may require slight modification to the code

## Wiring

The displays are connected to the corresponding  I2C pins of the multiplexer. So display 0 goes to SD0 & SC0 and so on.

![Multiplexer Chart](/img/Mux_Chart.jpg)

The rest should be fairly straight forward, but if not feel free to ask.

## To-Do
* Clean up the code
* Add comments
* Add a better wiring diagram
