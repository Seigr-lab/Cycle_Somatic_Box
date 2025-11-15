# Step 27: Comprehensive System Monitoring and Data Logging

## Objective

Establish continuous monitoring of all critical parameters (electrical output, temperature, moisture, pH) with data logging capabilities to track performance trends, identify optimization opportunities, and ensure long-term system health for your 200-400W Norwegian bioelectrical power station.

## Why This Matters

**Without monitoring, you're flying blind:**

- Can't tell if optimizations are working
- Don't detect problems until major failure
- Miss seasonal trends that could inform management
- Can't prove system performance to others (important for Seigr community knowledge sharing)

**With comprehensive monitoring:**

- Real-time visibility into all 55-115W of combined power output
- Early warning of issues (voltage drop, temperature crash, moisture imbalance)
- Historical data enables informed decisions (when to add compost, adjust moisture, refresh electrodes)
- **Validates** that your 2-4 unit system is hitting 200-400W target

## Monitoring Strategy

### **Three-Tier Monitoring Approach:**

**Tier 1: Manual spot checks (daily/weekly)**

- Visual inspection
- Handheld measurements (multimeter, thermometer, pH strips)
- **Effort:** 5-15 min/week
- **Cost:** €0 (using existing tools)
- **Good for:** Small-scale systems, budget-limited builds

**Tier 2: Continuous digital monitoring (recommended)**

- Arduino or Raspberry Pi datalogger
- Sensors for voltage, current, temperature, moisture
- **Logs data:** Every 5-60 minutes
- **Effort:** Initial setup 4-8 hours, then automated
- **Cost:** €50-150
- **Good for:** Serious optimization, multi-unit arrays, long-term studies

**Tier 3: Cloud-connected dashboard (advanced)**

- IoT platform (ThingSpeak, Blynk, Home Assistant)
- Remote access via smartphone/computer
- Alerts and automated control
- **Effort:** Setup 8-15 hours
- **Cost:** €80-250
- **Good for:** Remote cabins, advanced users, research documentation

**Recommendation for your cabin:** **Tier 2** (continuous logging) with optional Tier 3 (if internet available)

## Materials Needed

### **For Tier 1 (Manual Monitoring):**

**Already have from previous steps:**

- Multimeter (voltage, current, resistance)
- Thermometer probes
- pH test strips
- Moisture meter or squeeze test

**Additional (optional):**

- **Notebook or spreadsheet:** Log readings (€0)
- **Camera:** Document visual observations (smartphone)

### **For Tier 2 (Continuous Digital Monitoring):**

**Microcontroller/Computer:**

**Option A: Arduino (simpler, cheaper)**

- **Arduino Uno or Mega:** €15-30
- **Pros:** Simple programming, low power (can run 24/7 on 5V USB)
- **Cons:** Limited memory (can't store months of data locally)

**Option B: Raspberry Pi (more powerful)**

- **Raspberry Pi Zero 2 W or Pi 4:** €15-60
- **Pros:** Full Linux computer, WiFi, can host web dashboard, large storage (SD card)
- **Cons:** Higher power consumption (5-15W), more complex setup

**Recommendation:** Raspberry Pi Zero 2 W (€15, WiFi built-in, low power)

**Sensors:**

**Voltage sensors (for MFC and thermal output):**

- **Voltage divider modules or INA219 current/voltage sensors:** 2-4 pieces (€3-8 each)
  - Measure 0-48V DC
  - I2C or analog output to microcontroller
  - **Quantity:** One for MFC output, one for thermal output, one for combined 48V, one for EcoFlow input
- **Total:** €12-32

**Current sensors:**

- **ACS712 Hall-effect current sensor (5A or 20A version):** 2-4 pieces (€2-5 each)
  - Non-invasive (clamps around wire)
  - Measures DC current
- **Or: INA219 (combined voltage/current):** Recommended (€5-8 each)
- **Total:** €8-32

**Temperature sensors:**

- **DS18B20 digital temperature sensors (waterproof):** 4-8 pieces (€2-4 each)
  - 1-Wire protocol (multiple sensors on one pin)
  - Range: -55 to +125°C (perfect for compost)
  - **Locations:** Compost core (90cm depth), mid-zone (60cm), surface (30cm), ambient air, wall exterior, heat sink (TEG cold side)
- **Total:** €8-32

**Moisture sensor:**

- **Capacitive soil moisture sensor:** 2-4 pieces (€3-6 each)
  - Analog output (0-3.3V based on moisture)
  - Insert at different depths (30cm, 60cm, 90cm)
  - **Note:** These degrade over 6-12 months in compost (replaceable)
- **Total:** €6-24

**pH sensor (optional, expensive):**

- **Analog pH sensor module:** €20-50
  - Requires calibration, maintenance (buffer solutions)
  - **Alternative:** Continue manual pH testing (cheaper, adequate)

**Ambient sensors:**

- **DHT22 or BME280 (temperature + humidity + barometric pressure):** €5-15
  - Track outdoor weather correlation with system performance

**Total sensor cost:** €40-100

**Data Storage:**

**Arduino:** SD card module + microSD card (€5-10)
**Raspberry Pi:** microSD card (€8-20, 32-128GB)

**Power Supply:**

**5V USB power adapter:** €5-10 (powers Arduino or Raspberry Pi)
**Or:** 12V DC-DC buck converter (12V from system → 5V for datalogger) (€3-8)

- **Advantage:** Self-powered from bioelectrical system (nice Seigr touch!)

**Enclosure:**

**Waterproof project box (IP65):** €10-20

- Houses microcontroller and sensor connections
- Mounts near system

**Wiring and Connectors:**

**Jumper wires, terminal blocks, screw terminals:** €10-20
**Breadboard or protoboard (for sensor connections):** €5-10

**Total Tier 2 cost:** €90-200 (one-time investment, multi-year use)

### **For Tier 3 (Cloud Dashboard):**

**Add to Tier 2:**

- **Internet connection:** WiFi or cellular (€0 if cabin has internet, €15-30/month for cellular data plan)
- **IoT platform subscription:** Free tier usually sufficient (ThingSpeak, Blynk)
- **Optional: Custom domain/hosting:** €5-15/month (if want professional dashboard)

## Installation Process

### **Phase 1: Manual Monitoring Baseline (Week 1-4) - Tier 1**

**Even if planning Tier 2/3, start with manual monitoring to understand system:**

**1. Create monitoring log template:**

**Spreadsheet columns (Google Sheets, Excel, or paper notebook):**

```
Date | Time | MFC_V | MFC_I | Thermal_V | Thermal_I | Total_P | Temp_Core | Temp_Ambient | pH | Moisture | Leachate_L | Notes
-----|------|-------|-------|-----------|-----------|---------|-----------|--------------|----|----|----------|------
2025-11-15 | 09:00 | 2.8 | 0.6 | 6.2 | 2.1 | 68W | 48 | 12 | 7.1 | 60% | 1.2 | Baseline
```

**2. Daily measurements (first week):**

- **Time:** Same time each day (e.g., 9:00 AM) - eliminates time-of-day variation
- **MFC voltage/current:** Multimeter across MFC output (before boost converter)
- **Thermal voltage/current:** Across TEG bus
- **Total power to EcoFlow:** Read from EcoFlow display or volt-amp meter (Step 25)
- **Temperature:** Core temp (probe at 90cm depth), ambient (outdoor thermometer)
- **Time:** 10-15 minutes per day

**3. Weekly measurements:**

- **pH:** Leachate sample, test with strips
- **Moisture:** Squeeze test or meter reading at 3 depths (30cm, 60cm, 90cm), average
- **Leachate volume:** Measure daily drainage output, average per week

**4. Bi-weekly:**

- **Visual inspection:** Open access hatch, check for mold, pests, electrode exposure
- **Odor check:** Should be earthy, not foul

**5. Analyze first month of data:**

- **Look for trends:**
  - Is output increasing, stable, or declining?
  - Is temperature stable or fluctuating wildly?
  - Is moisture drifting toward dry or wet?
- **Correlations:**
  - Does output drop on cold days (temperature dependence)?
  - Does output spike after adding moisture (indicates was too dry)?
- **Baseline performance:**
  - Average power output: ___ W
  - Typical voltage/current ranges
  - Normal temperature: ___°C core,___ °C ambient

**Manual monitoring is sufficient for basic operation** - can stop here if budget-limited or satisfied with spot checks

### **Phase 2: Install Continuous Monitoring (Tier 2) - 6-10 hours**

**6. Select and acquire hardware:**

**Recommended starter kit:**

- Raspberry Pi Zero 2 W (€15)
- INA219 voltage/current sensors (×3): €24
- DS18B20 temperature sensors (×6): €18
- Capacitive moisture sensors (×3): €12
- BME280 ambient sensor: €8
- MicroSD card (32GB): €10
- USB power supply: €8
- Weatherproof enclosure: €15
- **Total:** ~€110

**7. Set up Raspberry Pi:**

**Install operating system:**

- Download Raspberry Pi OS Lite (headless, no desktop)
- Flash to microSD card (use Raspberry Pi Imager)
- Configure WiFi and SSH (remote access)
- Boot Pi, connect via SSH from computer

**Install Python libraries:**

```bash
sudo apt update
sudo apt install python3-pip python3-smbus i2c-tools
pip3 install adafruit-circuitpython-ina219 w1thermsensor RPi.GPIO
```

**8. Wire sensors to Raspberry Pi:**

**INA219 sensors (I2C, can chain multiple):**

- VCC → 3.3V (Pi pin 1)
- GND → Ground (Pi pin 6)
- SDA → GPIO 2 (Pi pin 3)
- SCL → GPIO 3 (Pi pin 5)
- **Address configuration:** Each INA219 has selectable I2C address (0x40, 0x41, 0x44, 0x45)
  - Sensor 1 (MFC): Address 0x40
  - Sensor 2 (Thermal): Address 0x41
  - Sensor 3 (Combined to EcoFlow): Address 0x44

**DS18B20 temperature sensors (1-Wire, all on one pin):**

- VCC → 3.3V
- GND → Ground
- Data → GPIO 4 (Pi pin 7)
- **4.7kΩ pull-up resistor** between Data and VCC (one resistor for all sensors)
- Each sensor has unique ID (auto-detected by Pi)

**Capacitive moisture sensors (analog, need ADC):**

- **Problem:** Pi has no analog inputs (Arduino has, Pi doesn't)
- **Solution:** Add MCP3008 ADC chip (8-channel, SPI interface) (€3-5)
- MCP3008 wiring:
  - VDD → 3.3V, GND → Ground
  - CLK → GPIO 11 (pin 23), MISO → GPIO 9 (pin 21), MOSI → GPIO 10 (pin 19), CS → GPIO 8 (pin 24)
  - CH0-CH2 → Moisture sensors (3 channels)

**BME280 ambient sensor (I2C):**

- VCC → 3.3V, GND → Ground
- SDA/SCL → Same I2C bus as INA219 (address 0x76 or 0x77, no conflict)

**9. Test sensors individually:**

**Python test script (INA219 example):**

```python
from adafruit_ina219 import INA219
import board
import busio

i2c = busio.I2C(board.SCL, board.SDA)
ina_mfc = INA219(i2c, addr=0x40)

print("MFC Voltage: {:.2f}V".format(ina_mfc.bus_voltage))
print("MFC Current: {:.0f}mA".format(ina_mfc.current))
print("MFC Power: {:.2f}W".format(ina_mfc.power / 1000))
```

**Run:** `python3 test_ina219.py`
**Expected:** Prints current MFC readings

**Repeat for all sensors** (verify each works before proceeding)

**10. Write main data logging script:**

**Python script (`bioelectric_logger.py`):**

```python
#!/usr/bin/env python3
import time
import csv
from datetime import datetime
from adafruit_ina219 import INA219
from w1thermsensor import W1ThermSensor, Unit
import board
import busio
# ... (add other sensor libraries)

# Initialize sensors
i2c = busio.I2C(board.SCL, board.SDA)
ina_mfc = INA219(i2c, addr=0x40)
ina_thermal = INA219(i2c, addr=0x41)
ina_total = INA219(i2c, addr=0x44)

temp_sensors = W1ThermSensor.get_available_sensors()
# Identify sensors by location (measure and record IDs during installation)
temp_core = W1ThermSensor(sensor_id="XXXXXXXXXXXX")  # Replace with actual ID
temp_ambient = W1ThermSensor(sensor_id="YYYYYYYYYYYY")

# CSV log file
log_file = "/home/pi/bioelectric_data.csv"

# Create header if new file
with open(log_file, 'a', newline='') as f:
    writer = csv.writer(f)
    if f.tell() == 0:  # Empty file
        writer.writerow(["Timestamp", "MFC_V", "MFC_I", "MFC_P", 
                         "Thermal_V", "Thermal_I", "Thermal_P",
                         "Total_V", "Total_I", "Total_P",
                         "Temp_Core", "Temp_Ambient", "Moisture_30cm"])

# Main logging loop
while True:
    try:
        timestamp = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
        
        # Read electrical
        mfc_v = ina_mfc.bus_voltage
        mfc_i = ina_mfc.current / 1000  # mA to A
        mfc_p = ina_mfc.power / 1000    # mW to W
        
        thermal_v = ina_thermal.bus_voltage
        thermal_i = ina_thermal.current / 1000
        thermal_p = thermal_v * thermal_i
        
        total_v = ina_total.bus_voltage
        total_i = ina_total.current / 1000
        total_p = total_v * total_i
        
        # Read temperatures
        temp_core_c = temp_core.get_temperature(Unit.DEGREES_C)
        temp_ambient_c = temp_ambient.get_temperature(Unit.DEGREES_C)
        
        # Read moisture (simplified, actual needs MCP3008 library)
        moisture = 60  # Placeholder
        
        # Write to CSV
        with open(log_file, 'a', newline='') as f:
            writer = csv.writer(f)
            writer.writerow([timestamp, mfc_v, mfc_i, mfc_p,
                           thermal_v, thermal_i, thermal_p,
                           total_v, total_i, total_p,
                           temp_core_c, temp_ambient_c, moisture])
        
        print(f"{timestamp}: Total {total_p:.1f}W, Core {temp_core_c:.1f}°C")
        
        time.sleep(300)  # Log every 5 minutes (300 seconds)
        
    except Exception as e:
        print(f"Error: {e}")
        time.sleep(60)  # Wait before retry
```

**11. Set script to run at boot:**

```bash
# Make executable
chmod +x bioelectric_logger.py

# Create systemd service
sudo nano /etc/systemd/system/bioelectric.service
```

**Service file content:**

```
[Unit]
Description=Bioelectric Monitoring
After=network.target

[Service]
ExecStart=/usr/bin/python3 /home/pi/bioelectric_logger.py
Restart=always
User=pi

[Install]
WantedBy=multi-user.target
```

**Enable service:**

```bash
sudo systemctl enable bioelectric.service
sudo systemctl start bioelectric.service
```

**Monitor is now running 24/7**, logging every 5 minutes (or adjust interval)

**12. Data visualization:**

**Option A: Retrieve CSV and plot on computer**

- SCP or SFTP to download `/home/pi/bioelectric_data.csv`
- Open in Excel, Google Sheets, or Python (Pandas, Matplotlib)
- Create time-series graphs

**Option B: Real-time dashboard on Pi (lightweight web server)**

- Install Flask or simple HTTP server
- Serve web page that reads CSV and plots with Chart.js or Plotly

### **Phase 3: Cloud Integration (Tier 3) - Optional, 4-6 hours**

**13. Set up ThingSpeak (free IoT platform):**

**Create account:** thingspeak.com (free)
**Create channel:**

- Fields: MFC_Power, Thermal_Power, Total_Power, Temp_Core, Temp_Ambient, Moisture
- Get Write API Key (used to send data)

**14. Modify Python script to upload data:**

```python
import requests

THINGSPEAK_KEY = "YOUR_API_KEY"
THINGSPEAK_URL = "https://api.thingspeak.com/update"

# Inside logging loop, after collecting data:
payload = {
    'api_key': THINGSPEAK_KEY,
    'field1': mfc_p,
    'field2': thermal_p,
    'field3': total_p,
    'field4': temp_core_c,
    'field5': temp_ambient_c,
    'field6': moisture
}
requests.post(THINGSPEAK_URL, data=payload)
```

**Now data is viewable from anywhere:** thingspeak.com/channels/YOUR_CHANNEL

**15. Set up alerts (if output drops):**

**ThingSpeak React:**

- Create alert: If Total_Power < 30W, send email
- Or: If Temp_Core < 25°C, alert (system is cooling, needs attention)

**16. Mobile access:**

**ThingSpeak mobile app** (iOS/Android) shows live charts

**Or:** Home Assistant integration (for advanced smart home users)

## Expected Results

**After monitoring system installation:**

**Data visibility:**
✅ **Real-time power output:** Visible at any time (manual check or dashboard)
✅ **Historical trends:** Days, weeks, months of performance data
✅ **Correlations identified:** Temperature vs output, moisture vs output, seasonal patterns
✅ **Early problem detection:** Output drop alerts before total failure

**Typical logged data (mature system, winter):**

```
2025-12-15 09:00: MFC 12W, Thermal 85W, Total 97W, Core 52°C, Ambient 5°C
2025-12-15 15:00: MFC 14W, Thermal 92W, Total 106W, Core 54°C, Ambient 8°C
2025-12-15 21:00: MFC 11W, Thermal 78W, Total 89W, Core 50°C, Ambient 2°C
```

**Insights from monitoring:**

- **Daily variation:** ±10-15W (normal, due to ambient temp changes)
- **Weekly trend:** Stable (indicates healthy system)
- **Monthly:** Slow increase as biofilm matures (first 3 months), then plateau
- **Seasonal:** Winter high (thermal excellent), summer lower (thermal reduced)

**Performance validation:**

- **Single unit:** 55-115W continuous (verified by data, not guesswork)
- **Multi-unit array (3 units example):** 165-345W combined
- **Achievement:** Meeting 200-400W target confirmed by logged data

## Troubleshooting

**"Raspberry Pi datalogger crashes or stops after a few days"**

- **SD card corruption:** Common issue (write-intensive logging)
  - **Fix:** Use higher-quality SD card (SanDisk, Samsung EVO)
  - **Or:** Log to USB drive instead of SD card
  - **Or:** Reduce logging frequency (every 15-30 min instead of 5 min)
- **Power supply insufficient:** Pi brownout (needs stable 5V, 2.5A)
  - **Fix:** Use quality power adapter

**"Sensors giving erratic readings"**

- **Loose wiring:** Check all connections (jumper wires can wiggle loose)
- **Interference:** Long sensor wires act as antennas (shorten or use shielded cable)
- **Moisture ingress:** Waterproof sensors failing (replace, ensure proper sealing)

**"Data shows output declining over weeks"**

- **This is the value of monitoring!** Early detection
- **Investigate:** Check temperature (cooling?), moisture (drying?), pH (acidifying?)
- **Correlate with manual observations:** Did you notice odor change, leachate color change?
- **Act based on data:** If temp dropped, add insulation; if moisture low, add water

**"Can't access cloud dashboard (ThingSpeak shows no data)"**

- **Internet connection:** Pi needs WiFi or ethernet
  - Check Pi connectivity: `ping 8.8.8.8`
- **API key wrong:** Verify ThingSpeak key in script
- **Rate limiting:** Free ThingSpeak has update limits (15 sec intervals minimum)

**"Monitoring shows huge power spikes (200W for few minutes, then back to 70W)"**

- **Sensor calibration issue:** INA219 reading incorrectly
  - **Fix:** Check sensor wiring, verify with multimeter (compare sensor reading to multimeter reading)
- **Actual spike:** Possible if large load suddenly removed from EcoFlow (system voltage rises temporarily)

## Connection to Next Steps

**Step 27 outputs (monitoring data) enable:**

**→ Step 28 (Daily Operation):**

- Dashboard shows real-time status (can decide when to run heavy loads based on available power)
- Alerts notify if system needs attention (before you notice manually)

**→ Step 29 (Long-term Optimization):**

- Historical data reveals optimization opportunities (e.g., "output always drops on Thursdays" → investigate pattern)
- Can test optimizations scientifically (change one variable, measure result)

**→ Step 30 (Maintenance):**

- Degradation trends visible early (gradual output decline signals upcoming maintenance needs)
- Can schedule maintenance based on data (e.g., "every 6 months, output drops 20%" → proactive refresh)

**Monitoring transforms system from black box to transparent, data-driven operation!**

---

**Time investment:**

- Tier 1 (manual): 10-15 min/week ongoing
- Tier 2 (continuous): 6-10 hours setup, then automated
- Tier 3 (cloud): +4-6 hours setup

**Materials cost:**

- Tier 1: €0 (existing tools)
- Tier 2: €90-200
- Tier 3: €0-15/month (cloud services)

**Value:** Priceless (data-driven operation, early problem detection, performance validation)

**Next:** Step 28 - Integrate bioelectrical power into daily cabin operations!
