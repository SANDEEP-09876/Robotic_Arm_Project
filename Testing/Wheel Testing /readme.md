# Run by using http://10.11.78.153  replace the ip address

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

# Left Driver Connections

| NodeMCU | Left Driver |
|----------|-------------|
| D1 | DIR1 orange |
| D2 | PWM1 yellow|
| D3 | DIR2 white|
| D4 | PWM2 red |

# Right Driver Connections

| NodeMCU | Right Driver |
|----------|--------------|
| D5 | DIR1 orange |
| D6 | PWM1 yellow |
| D7 | DIR2 white |
| D8 | PWM2 red |

# Notes

- Left driver controls both left motors
- Right driver controls both right motors
- Connect all grounds together
- Use external battery for motors
