<h1> It uses Google Genai by api key <h1>


To ensure your robotic assistant functions reliably, you must connect the NodeMCU, PCA9685 servo driver, and SmartElex motor driver using a Common Ground strategy. This prevents signal noise and communication errors between the different subsystems.1. PCA9685 Servo Driver to NodeMCUThis connection uses the I2C protocol to control all 5 joints of your robotic arm.PCA9685 PinNodeMCU PinDescriptionVCCVIN (recommended)Logic power (using VIN provides a stable 5V from USB)GNDG (GND)Common ground referenceSDAD2 (GPIO 4)I2C Data lineSCLD1 (GPIO 5)I2C Clock lineExternal Power: Connect your 5V/6V battery to the Green Screw Terminal on the PCA9685. Do not power the servos directly from the NodeMCU.2. SmartElex Motor Driver to NodeMCUThis handles the high-speed PWM signals for your differential drive base.SmartElex PinNodeMCU PinFunctionL_PWMD7 (GPIO 13)Left Motor SpeedL_DIRD3 (GPIO 0)Left Motor DirectionR_PWMD8 (GPIO 15)Right Motor SpeedR_DIRD4 (GPIO 2)Right Motor DirectionGNDG (GND)Connect to the same Ground as the PCA96853. Critical Wiring TipsThe Golden Rule of Grounding: You must connect a wire between the GND of the NodeMCU, the GND of the PCA9685, and the GND of the SmartElex driver. Without this "Common Ground," your commands will be ignored or cause erratic twitching.Servo Orientation: When plugging your 5 servos into the PCA9685 (Channels 0–4), ensure the Brown/Black wire (Ground) is on the bottom row and the Yellow/Orange wire (Signal) is on the top row.Ultrasonic Sensor (Optional): If you decide to add it back for the autonomous safety check, connect Trig to D5 and Echo to D6 (using a resistor divider if necessary for 3.3V safety).

                                                                                                                                                                  SmartElex Pin,NodeMCU Pin,Function
L_PWM,D7 (GPIO 13),Left Motor Speed
L_DIR,D3 (GPIO 0),Left Motor Direction
R_PWM,D8 (GPIO 15),Right Motor Speed
R_DIR,D4 (GPIO 2),Right Motor Direction
GND,G (GND),Connect to the same Ground as the PCA9685           
                                                                                                                                                                                                                                                                                                                                     PCA9685 Pin,NodeMCU Pin,Description
VCC,VIN (recommended),Logic power (using VIN provides a stable 5V from USB)
GND,G (GND),Common ground reference
SDA,D2 (GPIO 4),I2C Data line
SCL,D1 (GPIO 5),I2C Clock line                                                                                                                                                           
