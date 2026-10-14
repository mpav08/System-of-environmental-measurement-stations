This is from the 8th semester project with the theme being a system of systems.

The objective of this project was trying to create a noise measurement model by using a electret microphone to record signal noises in an outdoor environment. 
By including other sensors to confirm environmental conditions which could attenuate sound LoRa is used to send all the necessary data as a 
packet to a Rasbperry Pi, which in turn receives the packet and breaks it into topics which will be published with MQTT to Node-RED.
Moreover the team also had to take into consideration GDPR rules which most of them were covered in a short period (6 months).

The ESP32 and the RPI both had LoRa antennas, as the ESP32 was programmed in Arduino IDE to convert noise signals to Sound Pressure Levels and A weighted SPL. By taking into account enviromental conditions such as temperature, humidity and air pressure the final measurements were sent to RPI which used a script to receive the data which would be uploaded to NODE-RED using MQTT.


Data can be seen from the NODE-RED dashboard and a worldmap to indicate the loudness of the area. Lastly all the data are locally saved to the 
Raspberry Pi in the form of a CSV file that includes a timestamp which could be used for further analysis.
