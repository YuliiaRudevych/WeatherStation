# Introduction

This project will help to make your own weather station at home. With one ESP32 board and 2 sensors, we will create a full-fledged weather station with 4 parameters: temperature, humidity, pressure and altitude. There will also be automation here, which will send a notification in the application when the temperature drops below or rises above the comfort level for the home, as well as about too high or too low humidity, which will help to make the microclimate at home comfortable.

# Components Used in This Project
* Blynk web dashboard and Blynk App for mobile dashboard
* ESP32 Dev Module
* DHT21/AM2301A humidity and temperature sensor
* Barometer BMP280 3.3V

# Prepare your Hardware 

For this tutorial, we need the ESP32 Dev Module board, two sensors: DHT21/AM2301A humidity and temperature sensor and
Barometer BMP280 3.3V (atmospheric pressure sensor) and USB cable to connect board to computer.
How to connect ESP32 to DHT21/AM2301A humidity and temperature sensor
*Picture*
You have to connect:
1. 5V to 5V in the ESP32
2. GND to GND in the ESP32
3. Data to IO25 in the ESP32

How to connect ESP32 to Barometer BMP280 3.3V (atmospheric pressure sensor)
*Picture*

#  Prepare required software

* Install PlatformIO
* Install Blynk library for PlatformIO and create new sketch:
  1. Open PlatformIO Home > “+ New Project”
  2. Add name, select hardware (I have Esp32 Dev Module), select Arduino framework, click "Finish"
  3. Open PlatformIO Home > Libraries
  4. Enter in the search "Blynk" and find this library
  5. Click on it and click "Add to project"
  6. Choose your project and click "Add"

# Prepare the Firmware and upload it to your device

Now you need to include TemplateID, AuthToken (unique identifier of your device) and WiFi credentials to the sketch. Follow next steps to do it.

* Click on the Activate device action in Template Home tab (this tab should open automatically once you've pressed the Use Blueprint button)
* Enter the Wi-Fi credentials your device will use
* Copy the sketch and paste it to the IDE
* Flash your device :
1. Open the "src" folder and open the "Main.cpp" file
2. Insert the code
3. Press "PlatformIO: Upload"
* The device should open automatically



# Next steps after the device is activated

* Explore the Blynk Web Console and Blynk IoT app, try controlling your device from both
* Explore Blynk Documentation and learn how to work with Virtual Pins
* Improve the code for your needs
* Add more devices


# Create automations
Automation templates are already created in the template, you just need to enable them.
To do this, you need to open the "automation" tab and on the right you will have a list of recommended automations. There will be 4 automations:
1. Send a notification if the temperature is above comfortable
2. Send notification if the temperature is below comfortable
3. Send notification if humidity is higher than comfortable
4. Send notification if the humidity is below comfortable

"Picture*
In order to add them, click on automation and click "Save" at the top. You can also change the temperature and humidity that are comfortable for you.

# Troubleshooting

* Make sure you have the latest Blynk Library installed
* Check that all the dependencies and configurations are correct
* Check your sketch for errors. Click the Verify button to compile your sketch without uploading it
* Check your board and port selections
* Check your connections. Your board needs to be connected with a data USB cable (charge-only cables will not work). Make sure the cable is fully inserted in the port on each end. Try a different USB cable, and avoid hubs and other adapters if possible. Remove connections to the board pins, especially the 0 (RX) and 1 (TX) digital pins.
* Check that your boards and libraries are up to date









