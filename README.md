# Robotic Arm Torque Calculation & Servo Selection

## 1. Torque Calculation for Each Joint

Given:
- Payload: **1 kg** → Force = 1 × 9.81 = **9.81 N**
- Link lengths:
  - Link 1: 15 cm = 0.15 m
  - Link 2: 10 cm = 0.10 m
  - Gripper: 4 cm = 0.04 m

### Torque formula:
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

### ✅ For Joint 1 (~28.4 kg·cm):
- **LewanSoul LX-224HV**
  - Torque: 20 kg·cm @ 11.1V (serial bus servo with feedback)
  - Might need a gearbox or higher torque version (e.g., LX-45 or DS3225 for safety)
  - [Amazon Link](https://www.amazon.com/LewanSoul-Connectors-Equipped-Position-Temperature/dp/B081CTX6DM)
  - [Hiwonder Link](https://www.hiwonder.com/products/lx-224hv)

### ✅ For Joint 2 (~13.7 kg·cm):
- **DS3218 Digital Servo**
  - Torque: 21.5 kg·cm @ 6.8V
  - Waterproof, metal gear, suitable for heavy-duty robotic arms
  - [Amazon Link](https://www.amazon.com/DS3218-Torque-Digital-Waterproof-Rotation/dp/B07FMBBPD2)

### ✅ For Joint 3 (~3.92 kg·cm):
- **MG996R or DS3218**
  - MG996R: ~11 kg·cm @ 6V (sufficient)
  - [Amazon Link](https://www.amazon.com/MG996R-Digital-Torque-Metal-Helicopter/dp/B07NQWWZ6Y)

---

## 3. If Payload = 2 kg
- All torque values double:
  - Joint 1: ~56.8 kg·cm
  - Joint 2: ~27.4 kg·cm
  - Joint 3: ~7.84 kg·cm

### Downsides:
- Higher power consumption
- Slower motion due to gear reduction
- Increased stress on joints and frame

### Solutions:
- Add a gearbox for torque amplification
- Use high-torque servos (e.g., LX-45HV or DS3225)
- Consider stepper motors with external drivers for very high torque

---

## 4. Purchase Links (Verified)
- **DS3218 (20–21.5 kg·cm):**
  - [Amazon DS3218](https://www.amazon.com/DS3218-Torque-Digital-Waterproof-Rotation/dp/B07FMBBPD2)
- **LewanSoul LX-224HV (20 kg·cm):**
  - [Amazon LX-224HV](https://www.amazon.com/LewanSoul-Connectors-Equipped-Position-Temperature/dp/B081CTX6DM)
  - [Hiwonder LX-224HV](https://www.hiwonder.com/products/lx-224hv)
- **MG996R (11 kg·cm):**
  - [Amazon MG996R](https://www.amazon.com/MG996R-Digital-Torque-Metal-Helicopter/dp/B07NQWWZ6Y)

---

## 5. Suggested Project Structure on GitHub

