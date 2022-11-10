# RaspberryPi Home Assistant temperature
[This projekt is work in progress]

# Materialeliste
* Raspberry Pi Zero v1.1 
* Displaytech 162C-BA-BC Reflective STN on Green - No Backlight

# Raspberry Pi
Raspberry Pi Zero(released in Nov 2015, by Raspberry Pi Foundation) is a single-board mini computer, mainly used to design embedded systems based IoT projects. The economical price, small-size and open-source design of this module makes it a suitable pick for applications ie. weather monitoring, motion-sensing camera, tiny power supply-sized computers and much more.

Ford Raspberry Pi zero er <u>meget</u> langsom med GUI og ssh remote brugte jeg en Raspberry Pi 4 brug i udviklingen. Når projektet kører lægges det over på en hedaless Zero.

## Header Pinout
![image](https://user-images.githubusercontent.com/44589560/201033305-a2e9fd92-64bc-4caa-b701-6893ce2832e2.png)

# Sensor
## Sensor pinout
![image](https://user-images.githubusercontent.com/44589560/201046656-42ed012c-920e-4456-a1e9-be1ae356d8e7.png)

# Display
![image](https://user-images.githubusercontent.com/44589560/201032597-428b1771-5aa2-4055-ab56-4708bc70bb10.png)
## Display pinout
![image](https://user-images.githubusercontent.com/44589560/201033586-71c464ba-d25c-4935-8331-9f7b48e4e9ec.png)
## Specs
* 16 x 2 Character LCD Displays
* Parallel interface
* KS0066U controller (COG versions use the NT603H controller)
* -10 °C to 60 °C operating temperature range

## Opsætning af display - 4 bit mode
![image](https://user-images.githubusercontent.com/44589560/201076605-e6c61200-0468-45b4-8d60-cc583db52ba1.png)

### Installering af Python bibliotek RPLCD
<code>sudo pip install RPLCD</code>

Hvis man oplever problemer med at få koden til at køre, kan man installere en ældre version

<code>pip install RPLCD==0.9</code>

Man kan teste om display er korrekt installeret og opsat med sanity check Hello, World!
<code>
from RPLCD import CharLCD

lcd = CharLCD(cols=16, rows=2, pin_rs=37, pin_e=35, pins_data=[33, 31, 29, 23])
lcd.write_string(u'Hello, World!')
</code>


## References
* https://docs.rs-online.com/6b5d/0900766b806dda16.pdf
* https://ie.rs-online.com/web/p/lcd-monochrome-displays/5326408
* https://www.pinteric.com/displays.html

# Homeassistant

## References
https://www.home-assistant.io/
