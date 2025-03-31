# IoT-Based AC Ceiling Fan Regulator  

## 📝 Description  
This project is an **IoT-based AC Ceiling Fan Regulator** that allows you to control the speed of your ceiling fan using an **Android application**. The circuit regulates fan speed by adjusting the **phase angle of the AC sine wave** using a **TRIAC**, controlled via **PWM signals** from an **ESP8266 (NodeMCU)**. The system integrates **Firebase Realtime Database** for cloud-based control, enabling remote adjustments via a mobile app.  

### 🔧 Key Features  
- **Wi-Fi Controlled** – Adjust fan speed remotely via an Android app.  
- **Phase Angle Control** – Uses TRIAC for efficient AC power regulation.  
- **Zero-Crossing Detection** – Ensures smooth switching and reduces noise.  
- **Firebase Integration** – Real-time updates for seamless control.  
- **Safe Isolation** – Optocouplers provide electrical isolation between high-voltage AC and low-voltage control circuits.  

## 🛠 Hardware Components  
| Component | Quantity |  
|-----------|----------|  
| ESP8266 (NodeMCU) | 1 |  
| NE555 Timer IC | 1 |  
| TRIAC (BT136) | 1 |  
| MOC3021 Opto-TRIAC Driver | 1 |  
| PC817 Optocoupler | 1 |  
| IRF9540 P-Channel MOSFET | 1 |  
| 1N4007 Diodes | 4 |  
| 56K, 1W Resistors | 2 |  
| 10K Resistors | 5 |  
| 82K Resistor | 1 |  
| 470Ω Resistors | 2 |  
| 47Ω Resistors | 2 |  
| 1000µF, 25V Capacitor | 1 |  
| 3.3µF Capacitor | 1 |  
| 0.1µF, 1KV Capacitor | 1 |  
| AMS1117-3.3V Regulator | 1 |  
| DC Power Jack | 1 |  
| Screw Terminal (5.04mm) | 2 |  

## 📡 Circuit Diagram & PCB Design  
The circuit consists of:  
1. **ESP8266 (Wi-Fi Control)** – Generates PWM for speed control.  
2. **Zero-Crossing Detector** – Provides sync for TRIAC triggering.  
3. **555 Timer (Monostable Mode)** – Controls TRIAC firing angle.  
4. **TRIAC & Snubber Circuit** – Regulates AC power to the fan.  
5. **Low-Pass Filter** – Converts PWM to analog for MOSFET control.  

🔗 **PCB Design**: Made in **Eagle CAD** (Gerber files available).  

## 📲 Software & Firebase Setup  
1. **Arduino IDE** – Used to program the ESP8266.  
2. **Firebase Realtime Database** – Stores fan speed values.  
3. **Android App** – Sends speed adjustments to Firebase.  

### 🔄 How Data Flow Works:  
- **Android App** → **Firebase DB** → **ESP8266** → **PWM Signal** → **555 Timer** → **TRIAC** → **Fan Speed Control**  

## ⚙️ Installation & Setup  
### 🔌 Hardware Setup  
1. Assemble the PCB as per the schematic.  
2. Connect **220V AC input** (ensure proper insulation).  
3. Power the circuit using a **3.3V DC supply**.  
4. Connect the fan to the output terminals.  

### 💻 Software Setup  
1. **Flash ESP8266** with the provided Arduino code.  
2. Configure **Firebase Realtime Database** and update credentials in the code.  
3. Install the **Android app** and link it to Firebase.  

## 📱 Android App Control  
- **Slider-based interface** for adjusting fan speed (0% to 100%).  
- Real-time updates via Firebase.  

## ⚠️ Safety Notes  
- **High Voltage Warning!** – This circuit works with **220V AC**. Handle with care.  
- Use proper **insulation** and **enclosure** for safety.  
- Ensure **correct grounding** to avoid electric shocks.  

## 📂 Repository Contents  
- `Circuit_Schematic/` – Eagle PCB design & Gerber files.  
- `Arduino_Code/` – ESP8266 Firebase & PWM control code.  
- `Android_App/` – APK or source code for the control app.  
- `Docs/` – Datasheets & additional references.  

## 🚀 Future Improvements  
- **Voice Control** (Alexa/Google Assistant integration).  
- **Multi-fan control** (Expandable to multiple channels).  
- **Energy Monitoring** (Track power consumption).  

## 📜 License  
**MIT License** – Open-source for educational & personal use.  

---

🌟 **Give it a ⭐ if you find this project useful!**  

---  
**Happy Building!** 🔧⚡  

---  <img width="1512" alt="Screenshot 2025-03-31 at 14 57 05" src="https://github.com/user-attachments/assets/94809bf9-860e-42e5-bd35-41f2dc1d90cc" />
<img width="1512" alt="Screenshot 2025-03-31 at 14 56 48" src="https://github.com/user-attachments/assets/ef075659-a1af-4141-bd8c-06989b5633bf" />


---
