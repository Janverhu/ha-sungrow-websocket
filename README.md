# Sungrow Home Assistant Integration

The Sungrow integration allows you to monitor and retrieve data from Sungrow solar inverters using the sungrow-websocket library.

## Installation

1. Install the sungrow-websocket library:

   ```shell
   pip install sungrow-websocket==0.2.2

2. Copy the custom_components/sungrow directory into your Home Assistant config/custom_components directory.
Configuration
To use this integration, add the following to your configuration.yaml file:

sensor:
  - platform: sungrow
    name: Your Sensor Name
    polling_interval: "00:05:00"  # Optional, set the desired polling interval
    sensors:
      sensor_id_1:
        ip: IP_ADDRESS_1
      sensor_id_2:
        ip: IP_ADDRESS_2

Replace Your Sensor Name, sensor_id_1, sensor_id_2, IP_ADDRESS_1, and IP_ADDRESS_2 with the appropriate values for your configuration.

Configuration Options
name (optional): The name for the Sungrow sensor. Default is "Sungrow Sensor".
polling_interval (optional): The interval at which the sensors will be polled for updates. Default is 5 minutes.
sensors (required): A dictionary of sensors to be monitored, where each key is a sensor ID and each value is the IP address of the corresponding Sungrow inverter.
Usage
The integration will create a sensor entity for each configured sensor ID. The state of each sensor entity will be the most recent data retrieved from the Sungrow inverter, and the attributes will include the full data dictionary.

Issues and Support
If you encounter any issues or have any questions or suggestions, please open an issue in the issue tracker for this integration.

License
This integration is licensed under the MIT License.