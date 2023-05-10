For this tutorial, we need the ESP32 Dev Module board and two sensors: DHT21/AM2301A humidity and temperature sensor and
Barometer BMP280 3.3V (atmospheric pressure sensor)

# Tutorial
This step-by-step tutorial will help you create your Weather Station in a very simple and clear way.
 # 1. Blynk Setup:
  1. Open https://blynk.io and log in
  2. Open "Templates" tab and click "+ New Template"
  3. Go to the "Datastreams" tab
  4. Create 4 Datastreams:
  * Virtual pin V0, Name "Temperature", Data type "Double", Units "Celsius", Min "-10", Max "45"
  * Virtual pin V1, Name "Humidity", Data type "Double", Units "Percentage", Min "0", Max "100"
  * Virtual pin V3, Name "Altitude", Data type "Double", Units "Meter", Min "0", Max "5000"
  * Virtual pin V4, Name "Pressure", Data type "Double", Units "Hectopascal", Min "0", Max "1070"
  5. Go to the "Web Dashboard" tab
  6. Add 5 Widgets:
  * Label, Title "Temperature", Datastream "Temperature V0", Show Level - On, Level Position "Vertical"
  * Label, Title "Humidity", Datastream "Humidity V1", Show Level - On, Level Position "Vertical"
  * Label, Title "Altitude", Datastream "Altitude V3", Show Level - On, Level Position "Vertical"
  * Label, Title "Pressure", Datastream "Pressure V4", Show Level - On, Level Position "Vertical"
  * Chart, Title "", Datastreams : 1. Temperature V0, Show Y-axis - On, Autoscale - On, 2. Humidity V1, Show Y-axis - On, Autoscale - On
  7. Add new tab for dashboard named "Historical Data"
  8. Add there 3 wadgets:
  * Heatmap Chart, Title "Heatmap", Datastreams: 1. Temperature V0, Show datastream name - On, Enable Zoom - On
  * Chart, Title "Temperature", Datastreams : 1. Temperature V0, Show Y-axis - On
  * Chart, Title "Humidity", Datastreams : 1. Humidity V1, Show Y-axis - On
  9. Click "Save and Apply"
  10. Go to the "Search-> My devices" tab
  11. Click "+ New Device", choose "From Template" and add name, choose "Weather Station" template.
  12. Click "Save". Device created!
  
  # 2. Coding
  1. Open Visual Studio Code
  2. Install PLatformIO : https://platformio.org
  3. Open "PlatformIO Home" and create new project 
  4. Add name, choose board (I have Esp32 Dev Module) and click "Finish"
  5. Open "src" folder and open "Main.cpp" file
  6. Insert code
  7. Press "PlatformIO: Upload"
  
 # Done!
