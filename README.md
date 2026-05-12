# SmartElex Motor Driver Connections

| SmartElex Pin | NodeMCU Pin | Function |
|----------------|-------------|----------|
| L_PWM yellow | D7 (GPIO13) | Left Motor Speed |
| L_DIR white | D3 (GPIO0) | Left Motor Direction |
| R_PWM | D8 (GPIO15) | Right Motor Speed |
| R_DIR | D4 (GPIO2) | Right Motor Direction |
| GND | G (GND) | Common Ground |

---

# PCA9685 Connections

| PCA9685 Pin | NodeMCU Pin | Description |
|--------------|-------------|-------------|
| VCC | VIN | Logic Power |
| GND | G (GND) | Common Ground |
| SDA | D2 (GPIO4) | I2C Data |
| SCL | D1 (GPIO5) | I2C Clock |
