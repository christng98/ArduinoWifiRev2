# ArduinoWifiRev2

En liten introduksjon til [Arduino WIFI Rev2](https://www.baldengineer.com/arduino-uno-wifi-rev-2-features-i-noticed.html).

For å koble Arduino Uno WIFI Rev2 til internett er det gunstig å koble til alt annet enn Eduroam. For eksempel internettdeling via mobildata eller et privat nettverk. 

En guide som kan brukes for å prøve å kommunisere med mikrokontrolleren finner man på [hjemmesiden](https://www.arduino.cc/en/Guide/ArduinoUnoWiFiRev2). 

[WoolseyWorkshop](https://www.woolseyworkshop.com/) har også en guide for å [kommunisere via en nettside](https://www.woolseyworkshop.com/2018/12/07/controlling-an-arduino-uno-wifi-rev2-or-arduino-uno-with-wifi-shield-from-a-web-browser/), og hvordan [hente data fra IMU](https://www.woolseyworkshop.com/2019/01/23/accessing-the-imu-on-the-new-arduino-uno-wifi-rev2/).

For det innebygde akselerometeret blir alt målt i **g**, hvor 1g = 9.81m/s^2 (med forbehold om avvik).
For det innebyde gyroskopet blir alt målt i **deg/s**, som er grader per sekund.
# Problemer underveis

Underveis har det dukket opp en del problemer. Noen var enklere å løse enn andre og her vil det bli nevnt noen som har dukket opp. Det oppfordres til å søke på nettet om du støter på problemer:

- [arduino.stackexchange](https://arduino.stackexchange.com/)
- [forum.arduino](https://forum.arduino.cc/index.php?board=126.0)
- [google](www.google.com)

Problemer:
- **Serial.print()** skriver ikke ut det du forventer til **Serial monitor**:
  - Sørg for at koden faktisk kan kompileres. Deretter sørg for at baud rate i **Serial monitor** er lik det du har i **Serial.begin(*baud rate*)** under **setup()**.
- Kan ikke laste inn angitt IP-adresse fra **Serial monitor** i Chrome eller Firefox:
  - Sørg for at datamaskinen er koblet til samme nettverk som Arduinoen før du laster inn siden igjen.

# MySQL og WiFi Rev2

WiFi Rev2 er ganske nytt, og det finnes kode som halvveis fungerer. Det er fortsatt ikke sikkert at [biblioteket](https://github.com/ChuckBell/MySQL_Connector_Arduino) fungerer for dette kortet (28.06.19). ([Se her](https://github.com/ChuckBell/MySQL_Connector_Arduino/issues/80)) Men prøv!
