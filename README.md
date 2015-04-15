# Color Temperature
SmartThings can set your lights to a specific color temperature, if you give it the exact right co-ordinates on CIE space. Unfortunately, this is an unnecessarily complicated thing and SmartThings doesn't actually support it out of the box. 

Color Temperature is a curve in X,Y co-ordinatesthrough CIE 1931.  It's exact position can change depending on a blackbody calibration -- most implementations including this one use D65. 

![1024px-planckianlocus](https://cloud.githubusercontent.com/assets/478212/7158851/85956888-e343-11e4-9109-f3756679b575.png)

This app, which is really just a template for your implementations, lets you specify a mode and a color temperature.  When SmartThings enters that mode, this app will change the color temperature of your lights accordingly. 

The bulk of this application is the translation from color temperature to RGB space, and then another conversion from RGB to HSB.  Both of these conversions need to be done as SmartThings expects any device with capability.colorControl to supply a Hue, Saturation and Brightness value (which then in turn gets converted back to Hex for the UI color wheel).

This application has been tested and verified with a color meter with the following bulbs:
  * Philips Hue LCT001, LCT002, LCT003
  * Osram 73674
  * LIFX A21E2

License
-------
Copyright (c) 2015, Kristopher Kubicki
All rights reserved.

