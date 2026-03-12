# F1-Marshal-Panel
F1 marshal LED panel using an ESP8266 (ESP-01) and a WS2812B 8×8 LED panel .

I built a small project that simulates an F1 marshal LED panel using an ESP8266 (ESP-01) and a WS2812B 8×8 LED panel . The panel is connected to Home Assistant and automatically displays the current track status from the entity sensor.f1_session_track_status .

The goal of the project was to create a decorative but also functional panel that reacts to the track status during a race, similar to the real panels used in Formula One.

Panel functions
CLEAR – green light (automatically turns off after 10 seconds)
YELLOW – yellow warning pattern
RED – red flashing
SC (Safety Car) – white SC letters with a rotating amber beacon cone around the panel border
VSC (Virtual Safety Car) – alternating V and SC letters with an amber frame
The panel also includes several additional features:

a boot animation when the device starts
a brightness slider in Home Assistant (10–70%)
automatic shutdown if no data is received from Home Assistant for 30 seconds
test buttons in Home Assistant for manually triggering all effects
Hardware
ESP8266 ESP-01
WS2812B 8×8 LED panel (64 LEDs)
5V power supply
The LED matrix is addressed as a serpentine 8×8 panel .

Software
The firmware is written in ESPHome , and the track status is received directly from Home Assistant through the sensor:

sensor.f1_session_track_status

All visual effects are implemented using the addressable_lambda feature to control each LED individually.

Project idea
While watching races, I wanted a small panel that visually shows the current track status in real time, similar to the marshal panels used around the circuit during Formula 1 events.

The result is a small F1 marshal panel simulator that integrates nicely into a smart-home setup.

[quote="SavSim, post:1, topic:995226"]
Many thanks to [Stimo Niklas](https://community.home-assistant.io/u/stimo/summary) for the [Formula 1 Racing Sensor](https://community.home-assistant.io/t/formula-1-racing-sensor/880842) .
[/quote]

