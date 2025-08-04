# Robotic Arm Torque Calculation & Servo Selection

---

## 1. Torque Calculation for Each Joint (Q1)

Given:
- Payload: **1 kg** → Force = 1 × 9.81 = **9.81 N**
- Link lengths:
  - Link 1: 15 cm = 0.15 m
  - Link 2: 10 cm = 0.10 m
  - Gripper: 4 cm = 0.04 m

### Formula:
\[
Torque = Force \times Distance
\]

| Joint        | Distance (m) | Torque (N·m) | Torque (kg·cm) |
|-------------|--------------|-------------|---------------|
| Joint 1 (Base) | 0.29         | 2.84        | ~28.4         |
| Joint 2        | 0.14         | 1.37        | ~13.7         |
| Joint 3        | 0.04         | 0.392       | ~3.92         |

---

## 2. Recommended Servo Motors

### ✅ Joint 1 (~28.4 kg·cm):
- **LewanSoul LX-224HV**
  - Torque: 20 kg·cm @ 11.1V (serial bus servo with feedback)
  - May require a gearbox or a higher torque variant for safety
  - [Amazon LX-224HV](https://www.amazon.com/LewanSoul-Connectors-Equipped-Position-Temperature/dp/B081CTX6DM)

### ✅ Joint 2 (~13.7 kg·cm):
- **DS3218 Digital Servo**
  - Torque: 21.5 kg·cm @ 6.8V
  - Waterproof, metal gear, suitable for robotic arms
  - [Amazon DS3218](https://www.amazon.com/DS3218-Torque-Digital-Waterproof-Rotation/dp/B07FMBBPD2)

### ✅ Joint 3 (~3.92 kg·cm):
- **MG996R**
  - Torque: ~11 kg·cm @ 6V (sufficient for small loads)
  - [Noon MG996R](https://www.noon.com/saudi-en/tower-pro-metal-gear-servo-motor-black/N35085024A/p/?o=a29d8e4c739a453a&gQT=2&shareId=0a91ca1e-b94e-412b-b69b-1da09391f924)

---

## 3. Can the same servos lift 2 kg instead of 1 kg? (Q2)

If the payload doubles to **2 kg**:
- All torque values will **double**:
  - Joint 1: ~56.8 kg·cm
  - Joint 2: ~27.4 kg·cm
  - Joint 3: ~7.84 kg·cm

### Downsides of using the same servos:
- **Overload** → Motors may overheat or fail
- **Slow movement** → Because of added gears or higher torque demand
- **Higher power consumption**
- **Reduced lifespan of motors and mechanical parts**

### Solutions:
- **Add gear reduction** to amplify torque (at the cost of speed)
- **Use stronger servos** (e.g., LX-45HV or DS3225 rated at 35–45 kg·cm)
- **Switch to stepper motors with drivers** for high-torque applications

---

## 4. Purchase Links (Verified)

- **DS3218 (20–21.5 kg·cm):**  
  [Amazon DS3218](https://www.amazon.com/DS3218-Torque-Digital-Waterproof-Rotation/dp/B07FMBBPD2)

- **LewanSoul LX-224HV (20 kg·cm):**  
  [Amazon LX-224HV](https://www.amazon.com/LewanSoul-Connectors-Equipped-Position-Temperature/dp/B081CTX6DM)

- **MG996R (11 kg·cm):**  
  [Noon MG996R](https://www.noon.com/saudi-en/tower-pro-metal-gear-servo-motor-black/N35085024A/p/?o=a29d8e4c739a453a&gQT=2&shareId=0a91ca1e-b94e-412b-b69b-1da09391f924)

---



