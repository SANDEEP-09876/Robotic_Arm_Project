You are using:

* 2 SmartElex dual-channel motor drivers
* Left side:
    * both left motors connected to Driver 1
    * using PWM1 + PWM2 together
    * using DIR1 + DIR2 together
* Right side:
    * both right motors connected to Driver 2
    * using PWM1 + PWM2 together
    * using DIR1 + DIR2 together

So each side needs:

* 2 PWM pins
* 2 DIR pins

Total:

* 8 ESP8266 pins
