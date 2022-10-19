# openHASP Mushroom-like cards

Here is my personal configuration for openHASP, using a 320x480 TFT lcd from a Wirelass Tag module (wt32-sc01).
All of the look/feel inspired by the excellent Mushroom cards for Home Assistant.

## How to use

[Set up openHasp](https://www.openhasp.com/0.6.3/getting-started/) on your device. Select material dark as your theme

If you just want to see how it looks on the device, [copying the content of pages.jsonl](https://www.openhasp.com/0.6.3/faq/#is-there-a-file-browser-built-in) to the microcontroller should be enough to get you started.

For a more complete installation, you will need to integrate the content of configuration.yaml to your own configuration.yaml, with taking care to replace all the entities id with your own.

## Setting up the page3 Timer functionality

Make sure you've completed the previous steps before proceeding, or copy the relevent section from configuration.yaml

 1. Create a dropdown helper with all the names of your entities you want to be able to control with a timer. This can also include groups. The last item in the dropdown should be "(none)" or "Nothing Selected", as we will default to that item

 2. Create a new Script in Home Assistant. I named my script plate02_settimer. Use the content from the included scripts.yaml. Replace all the entities name in the script.

 3. Create a Number helper named input_number.plate02_timer_hour with a minimum value of 0

 4. Create a Number helper named input_number.plate02_timer_minute with a minimum value of 0 and a maximum of 59

## Design/Style guide

The cards were designed for a 320x480 TFT lcd in portrait mode. The status bar is 35pixel high while the footer navigation is 45 pixels, leaving 400 pixels for content. The cards I have built try to stick to 80pixels in height whenever possible, but allowing for 40pixels and 120pixels cards too




ps: media controls for the Samsung TV on page 2 aren't implemented

## Screensots

page 1

![alt text](assets/page1.jpg)

page 2

![alt text](assets/page2.jpg)

page 3

![alt text](assets/page3.jpg)

page 4

![alt text](assets/page4.jpg)
