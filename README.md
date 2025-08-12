
OVERVIEW:
Sensors continuously capture environmental data.
ATmega328P processes data and calculates AQI.
AQI and pollutant data displayed in real-time.
If AQI > 100 → Microcontroller triggers fan + HEPA filter.
System resets AQI evaluation after purification.

Title: Pollution Monitoring System using ESP32


---

 Introduction:
- Air and noise pollution are serious environmental problems.
- This system monitors:
  - *Air Quality (MQ135)*
  - *Temperature & Humidity (DHT22)*
  - *Dust (PM2.5 - GP2Y1010AU0F)*
- Results displayed on OLED and sent over Bluetooth.

---

Components Used:
- ESP32 Development Board
- MQ-135 Gas Sensor
- DHT22 Temperature & Humidity Sensor
- GP2Y1010AU0F PM2.5 Dust Sensor
- SSD1306 OLED Display (128x64 I2C)
- Passive Buzzer
- Jumper Wires, Breadboard/PCB

---

Circuit Diagram:
- ESP32 pin connections:
  - MQ135 → GPIO 34 (Analog)
  - DHT22 → GPIO 14 (Digital)
  - GP2Y1010 Vo → GPIO 35 (Analog)
  - GP2Y1010 LED → GPIO 13 (Digital)
  - Buzzer → GPIO 4
  - OLED → I2C (SDA: 21, SCL: 22)
- Power Supply:
  - 5V for MQ135 and Dust Sensor
  - 3.3V for OLED, DHT22

---

Working Principle:
- *MQ135* detects harmful gases → gives analog value
- *DHT22* measures temp & humidity → via digital output
- *GP2Y1010AU0F* detects dust particles using LED pulse method
- *ESP32* processes data:
  - Shows on OLED
  - Sends via Bluetooth
  - Activates buzzer on high PM2.5 levels

---
OLED Display Output:
Shows:
- Temperature (°C)
- Humidity (%)
- Air Quality (Good/Medium/Bad)
- Raw MQ135 Value
- PM2.5 Dust (ug/m3)

---

Bluetooth Output:
Sends report to smartphone:

---- Pollution Report ----
Temp: 28.3 C
Humidity: 65.4 %
Air: Medium (1724)
PM2.5: 112 ug/m3
--------------------------


---

Applications:
- Smart cities
- Air quality monitoring for homes/schools
- Industrial pollution analysis
- Environmental research

---

Advantages:
- Low-cost and portable
- Real-time data monitoring
- Bluetooth wireless output
- Visual + audio alerts

---

Conclusion:
- This system provides a smart, real-time pollution monitoring solution.
- Helps create awareness and take action against pollution.

---
