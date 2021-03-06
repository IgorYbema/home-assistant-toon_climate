[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg)](https://github.com/custom-components/hacs)  [![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/) [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.me/cyberjunkynl/)

This is a Custom Component for Home-Assistant (https://home-assistant.io) that provides a climate device for rooted TOON thermostats.

You can read and control thermostat mode and presets, read current temperature and control the setpoint.

NOTE: This component only works with rooted TOON devices.
TOON thermostats are available in The Netherlands and Belgium.

More information about rooting your TOON can be found here:
[Eneco TOON as Domotica controller](http://www.domoticaforum.eu/viewforum.php?f=87)

{% if not installed %}

## Installation

- Install this integration using HACS.
- Configure using configuration instructions below.
- Restart Home-Assistant.

{% endif %}

## Usage
To use this component in your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry

climate:
  - platform: toon_climate
    name: TOON Thermostat
    host: IP_ADDRESS
    port: 10080
    scan_interval: 10
```

Configuration variables:

- **name** (*Optional*): Name of the device. (default = 'TOON Thermostat')
- **host** (*Required*): The IP address on which the TOON can be reached.
- **port** (*Optional*): Port used by your TOON. (default = 10080)
- **scan_interval** (*Optional*): Number of seconds between polls. (default = 60)

## Screenshot

![alt text](https://github.com/cyberjunky/home-assistant-toon_climate/blob/master/screenshots/toon.png?raw=true "Screenshot TOON")

TOON with simple-thermostat in Lovelace

![alt text](https://github.com/cyberjunky/home-assistant-toon_climate/blob/master/screenshots/toon-simple.png?raw=true "TOON simple-thermostat Screenshot")

Using this card:
```
   - type: 'custom:simple-thermostat'
     entity: climate.toon
     control:
       - preset
```

You can also control it with Google's assistant

![alt text](https://github.com/cyberjunky/home-assistant-toon_climate/blob/master/screenshots/toon-setpoint.png?raw=true "TOON Assistant Setpoint")
![alt text](https://github.com/cyberjunky/home-assistant-toon_climate/blob/master/screenshots/toon-eco-preset.png?raw=true "TOON Assistant ECO Preset")

## Donation
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.me/cyberjunkynl/)
