#

![simplinnovation](https://4.bp.blogspot.com/-f7YxPyqHAzY/WJ6VnkvE0SI/AAAAAAAADTQ/0tDQPTrVrtMAFT-q-1-3ktUQT5Il9FGdQCLcB/s350/simpLINnovation1a.png)

# Arduino MKR1000 & Blynk

### A simple IoT (Internet of Things) experiment using __Arduino/Genuino MKR1000__ and __Blynk__. Watch the video below ([click here](https://www.youtube.com/watch?v=MLUeEc9N6TM)) to see its action, then follow the instructions to build your own!

#

[![Video MKR1000 Blynk](https://img.youtube.com/vi/MLUeEc9N6TM/0.jpg)](https://www.youtube.com/watch?v=MLUeEc9N6TM)

#

### **1. What You Need** :gift:

To build this project, you need the following items:
- 1 Arduino/Genuino MKR1000 board
- 2 LEDs
- 1 Potentiometer
- Arduino IDE ([download here](https://www.arduino.cc/en/Main/Software))
- Blynk mobile app 
  - Android ([download here](https://play.google.com/store/apps/details?id=cc.blynk))
  - iOS ([download here](https://itunes.apple.com/us/app/blynk-control-arduino-raspberry/id808760481?ls=1&mt=8))
- WiFi101 library ([read how to install here](https://www.arduino.cc/en/Reference/WiFi101))
- Blynk library ([download here](https://github.com/blynkkk/blynk-library/releases/tag/v0.5.3))

#

### **2. Setup Blynk App** :iphone:

- Open Blynk app, login then create a new project. Choose device: __Arduino MKR1000__ with connection type: __WiFi__. Click __Create__ button & you will receive __Blynk Auth Token__ by email.

- On your project, add 2 button widget & a gauge. Set each widget as the picture below.

  ![Blynk App](https://raw.githubusercontent.com/LintangWisesa/Arduino_MKR1000_Blynk/master/Blynk_App.png)

#

### **3. Schematics** :wrench::hammer:

- Connect your parts to Arduino MKR1000 as the following picture:

  ![ArduinoMKR1000 Blynk schematics](https://raw.githubusercontent.com/LintangWisesa/Arduino_MKR1000_Blynk/master/Schematics.png)

#

### **4. Sketch** :clipboard:
 
- First, extract _**Blynk**_ library then copy it to _C:\\...\Documents\Arduino\libraries_.

- Open Arduino IDE then copy sketch below. Insert your WiFi SSID, WiFi password & Blynk Auth Token. Make sure you have chosen the right option for **_Board_** and **_Port_** under **_Tools_** menu. Upload it!

    ```c++
    #define BLYNK_PRINT SerialUSB
    #include <SPI.h>
    #include <WiFi101.h>
    #include <BlynkSimpleWiFiShield101.h>

    char auth[] = "Blynk_Auth_Token";
    char ssid[] = "Your_WiFi_Name";
    char pass[] = "Your_WiFi_Password";

    void setup(){
        SerialUSB.begin(9600);
        Blynk.begin(auth, ssid, pass);
    }

    void loop(){
        Blynk.run();
    }
    ```

#

### **5. Have Fun!** :sunglasses:

- After uploading done, make sure your Arduino MKR1000 & smartphone has a good internet connection. Click play button :arrow_forward: on top right corner of your Blynk project, then you're ready to go! Have fun! 

#

#### Lintang Wisesa :love_letter: _lintangwisesa@ymail.com_

[Facebook](https://www.facebook.com/lintangbagus) |
[Twitter](https://twitter.com/Lintang_Wisesa) |
[Google+](https://plus.google.com/u/0/+LintangWisesa1) |
[Youtube](https://www.youtube.com/user/lintangbagus) | 
:octocat: [GitHub](https://github.com/LintangWisesa) |
[Hackster](https://www.hackster.io/lintangwisesa)

