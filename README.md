# GroveMonitor (Monitor Side)
An IoT application using Raspberry Pis to create a full greenhouse monitoring solution. The system consists of a main RPi which communicates through socketio with the server and the other RPis. The other RPis either gather sensor data or activate relays using a PiFace.<br> The whole system consists of the following RPis:<br><br>
<strong>Main Raspberry:</strong><br>
-Gathers all the data collected from the other RPis and stores it/passes it to the server.<br>
-Serves a local webserver.<br>
-Gathers user defined values from the server (eg. variable thresholds, name, etc.) <br>
-Compares gathered data with the established thresholds and sends commands to activate relays to the respective RPis.<br><br>
<strong>Environment Monitor</strong> <br>
-Has the following sensors: Environment Temperature, Relative Humidity, Luminance, CO2 <br>
-Takes routine readings and passes them to the Main RPi <br>
-Takes readings based on the Main RPi's commands <br><br>
<strong>Nutrient Solution Monitor</strong> <br>
-Has the following sensors: Water Temperature, pH, EC, DO <br>
-Takes routine readings and passes them to the Main RPi <br>
-Takes readings based on the Main RPi's commands <br><br>
<strong>Environment Actuator</strong><br>
-Receives commands from the Main RPi and activates relays through the PiFace to Cool/Heat the environment (various stages) <br><br>
<strong>Nutrient Solution Actuator</strong><br>
-Receives commands from the Main RPi and activates relays through the PiFace to adjust pH and EC<br><br>



