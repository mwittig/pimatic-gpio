pimatic gpio plugin
=======================
Actuators and sensors for the raspberry pi gpio pins.

Configuration
-------------
You can load the plugin by editing your `config.json` to include:

    { 
       "plugin": "gpio"
    }

in the `plugins` Array. For all configuration options see 
[sispmctl-config-shema](sispmctl-config-shema.html)

Actuators can be added bei adding them to the `actuators` Array in the config file.
Set the `class` attribute to `GpioSwitch`. For example:

    { 
      "id": "led-light",
      "class": "GpioSwitch", 
      "name": "led light",
      "gpio": 25 
    }

For actuator configuration options see the 
[actuator-config-shema](actuator-config-shema.html) file.

Sensors are added to the `sensors` Array.

    { 
      "id": "presents-sensor",
      "class": "GpioPresents", 
      "name": "motion detector",
      "gpio": 21 
    }
