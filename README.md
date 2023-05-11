# Overview
This step-by-step tutorial will help you create your Weather Station in a very simple and clear way. You will be able to monitor temperature, humidity, atmospheric pressure, and altitude!
# Toolchain
* Platformio IDE: Download and install the VSCode and Platformio IDE 
* Blynk library for PlatformIO
* Adafruit BMP280 Library 
* DHT sensor library
# Components Used in This Project
* Blynk web dashboard
* ESP32 Dev Module
* DHT21/AM2301A humidity and temperature sensor
* Barometer BMP280 3.3V
# Step-by-Step Guide
 ### 1. Blynk Dashboard Setup
* Open Blynk.Cloud and log in your account
* Open the "Templates" tab and click "+ New Template"
* Go to the "Datastreams" tab
* Create 4 Datastreams:
1. Virtual pin V0, Name "Temperature", Data type "Double", Units "Celsius", Min "-10", Max "45"
2. Virtual pin V1, Name "Humidity", Data type "Double", Units "Percentage", Min "0", Max "100"
3. Virtual pin V3, Name "Altitude", Data type "Double", Units "Meter", Min "0", Max "5000"
4. Virtual pin V4, Name "Pressure", Data type "Double", Units "Hectopascal", Min "0", Max "1070"
* Go to the "Web Dashboard" tab
* Add 5 Widgets:
1.Label, Title "Temperature", Datastream "Temperature V0", Show Level - On, Level Position "Vertical"
2.Label, Title "Humidity", Datastream "Humidity V1", Show Level - On, Level Position "Vertical"
3.Label, Title "Altitude", Datastream "Altitude V3", Show Level - On, Level Position "Vertical"
4.Label, Title "Pressure", Datastream "Pressure V4", Show Level - On, Level Position "Vertical"
5.Chart, Title "", Datastreams: 1. Temperature V0, Show Y-axis - On, Autoscale - On, 2. Humidity V1, Show Y-axis - On, Autoscale - On
* Add a new tab for Dashboard named "Historical Data"
* Add there 3 widgets:
1. Heatmap Chart, Title "Heatmap", Datastreams: 1. Temperature V0, Show datastream name - On, Enable Zoom - On
2. Chart, Title "Temperature", Datastreams: 1. Temperature V0, Show Y-axis - On
3. Chart, Title "Humidity", Datastreams: 1. Humidity V1, Show Y-axis - On
* Click "Save and Apply"
* Go to the "Search > My devices" tab
* Click "+ New Device", choose "From Template" and add a name, choose "Weather Station" template.
* Click "Save". Device created!


### 2. Installing the Blynk library and libraries for our sensors:
* Open Visual Studio Code
* Open PlatformIO Home > “+ New Project”
* Add name, select hardware (I have Esp32 Dev Module), select Arduino framework, click "Finish"
* Open PlatformIO Home > Libraries
* Enter in the search "Blynk" and find this library
* Click on it and click "Add to project"
* Choose your project and click "Add"
Perfect, Blynk library added! Lets add libraries for our sensors:
* Turn back to libraries
* Enter in the search "Adafruit BMP280 Library " and inslall it as in previous steps
* Enter in the search "DHT sensor library " and inslall it as in previous steps
Now that we've made all the necessary settings, let's finish by uploading the code to our board.


### 3. Uploading the code

* Open the "src" folder and open the "Main.cpp" file
* Insert the code
* Replace Template ID, Template Name, and Auth Token placeholders in the code. Find them in the Blynk Console > Device >Device Info > FIRMWARE CONFIGURATION window 
* Press "PlatformIO: Upload"

And that's it! Enjoy your own Weather Station!








