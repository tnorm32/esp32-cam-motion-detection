ESP32-CAM Motion Detection with Telegram Alerts (Energy Saver Version)

This project is based on the [ESP32-CAM PIR Kit from Lonely Binary](https://lonelybinary.com/products/esp32cam-pir-kit)
It uses an ESP32-CAM and PIR shield for motion detection, but has been modified to be a compact, low-power solution with extra hardware for portability.


**Features**
- PIR sensor acts as a pin interrupt → wakes the ESP32-CAM on motion.  
- Captures a picture and sends it to a Telegram bot.  
- Device then powers down to save energy.  
- Fully portable with LiPo battery + charging module + step-up voltage regulator (5V output).  
- On/off switch integrated.  
- Relocated the PIR interrupt pin to avoid conflicts with the serial monitor.


**Hardware Used**
- ESP32-CAM  
- ESP32-CAM PIR Kit shield (Lonely Binary)  
- LiPo battery  
- TP4056 charging module  
- Step-up voltage regulator (to 5V)  
- Toggle switch  


**How It Works**
1. Idle mode: ESP32-CAM stays off until PIR detects motion.  
2. Trigger: PIR interrupt powers the board → ESP32-CAM boots.  
3. Capture & Notify: Takes a picture, sends it through Telegram.  
4. Shutdown: ESP32-CAM powers down again, conserving battery.  


**Wiring Notes**
- PIR interrupt pin relocated to avoid serial monitor interference.  
- Power routed through step-up regulator for stable 5V operation.

Wiring diagram

<img width="628" height="527" alt="image" src="https://github.com/user-attachments/assets/bc15bf29-c3d0-4035-80e1-1c283ade299f" />


**Future Improvements**

 ☐ Add timestamps to captured photos  
 ☐ Integrate an external antenna for longer WiFi range  
 ☐ Implement AP (Access Point) mode:  
 ☐ Use an SD card for configuration storage (e.g., access point, camera settings such as flash, resolution, frame rate)  
 ☐ Enable local saving of photos to the SD card  


