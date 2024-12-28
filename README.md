# Air Monitoring System

This project uses an **MQ2** gas sensor to detect the concentration of **LPG** and **smoke** in the air, as well as monitoring **CO** (Carbon Monoxide) and **ARQ** values. The system displays the results on an LCD screen and triggers alarms using LEDs and a buzzer when dangerous gas levels are detected.

### Features:
- Detects LPG, smoke, CO, and ARQ levels.
- Displays sensor values on a 16x2 LCD screen.
- Triggers buzzer and LED indicators based on gas concentration levels.
- Real-time monitoring through serial communication.

### Components Used:
- **MQ2 Sensor** (for detecting LPG and smoke)
- **LCD 16x2** (I2C interface for display)
- **LEDs** (for indicating safety status)
  - Red LED (for warning)
  - Green LED (for safe status)
- **Buzzer** (for alerting the user)
- **Arduino Uno** or compatible board

### Circuit Connections:
- **MQ2 Sensor**: Analog input (A0).
- **LPG Sensor**: Analog input (A1).
- **Smoke Sensor**: Analog input (A2).
- **CO Sensor**: Analog input (A2).
- **Red LED**: Pin 12.
- **Green LED**: Pin 11.
- **Buzzer**: Pin 10.
- **LCD Display**: I2C connection (SCL, SDA).

### Installation:
1. Install **Arduino IDE** on your computer.
2. Install necessary libraries:
   - `MQ2` (for gas sensor)
   - `Wire` and `LiquidCrystal_I2C` (for LCD communication)
3. Connect the components as per the circuit description.
4. Upload the provided code to the Arduino board.

### Code Overview:
1. **MQ2 Gas Sensor**: Reads the gas concentrations for LPG, smoke, and other gases.
2. **LCD Display**: Displays sensor values for LPG, smoke, ARQ, and CO.
3. **Red and Green LEDs**: 
   - **Red LED** turns on if CO levels exceed a threshold.
   - **Green LED** indicates safe CO levels.
4. **Buzzer**: Sounds when dangerous levels of LPG or smoke are detected.
5. **Serial Monitor**: Prints the sensor values for debugging or monitoring purposes.

### Working:
- The system continuously reads values from the MQ2 sensor and other connected sensors.
- It displays the values for **LPG**, **smoke**, **CO**, and **ARQ** on the LCD screen.
- If **LPG** or **smoke** exceeds the defined threshold, the buzzer is activated.
- If **CO** levels exceed the threshold, the red LED is turned on, indicating a dangerous situation.
- If all readings are within safe limits, the green LED is displayed.

### Notes:
- The sensor values are calibrated for detecting LPG and smoke concentrations. Adjustments might be required based on your specific environment.
- You can adjust the `sensorThres` variable to change the threshold for triggering the alarm.

### License:
This project is open-source and available under the [MIT License](LICENSE).

