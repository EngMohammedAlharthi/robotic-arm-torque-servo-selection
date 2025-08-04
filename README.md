# Robotic Arm Torque Calculation & Servo Selection

## 1. Torque Calculation for Each Joint

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
  - May require a gearbox or higher torque variant for safety
  - [Amazon LX-224HV](https://www.amazon.com/LewanSoul-Connectors-Equipped-Position-Temperature/dp/B081CTX6DM)

### ✅ Joint 2 (~13.7 kg·cm):
- **DS3218 Digital Servo**
  - Torque: 21.5 kg·cm @ 6.8V
  - Waterproof, metal gear, suitable for robotic arms
  - [Amazon DS3218](https://www.amazon.com/DS3218-Torque-Digital-Waterproof-Rotation/dp/B07FMBBPD2)

### ✅ Joint 3 (~3.92 kg·cm):
- **MG996R**
  - Torque: ~11 kg·cm @ 6V (sufficient for small loads)
  - [Amazon MG996R](https://www.amazon.com/MG996R-Digital-Torque-Metal-Gear/dp/B00KKTR0TY)

---

## 3. If Payload = 2 kg
- Torque values double:
  - Joint 1: ~56.8 kg·cm
  - Joint 2: ~27.4 kg·cm
  - Joint 3: ~7.84 kg·cm

### Downsides:
- Higher power consumption
- Slower movement due to gear reduction
- More stress on joints and frame

### Solutions:
- Add a gearbox for torque amplification
- Use high-torque servos (e.g., LX-45HV or DS3225)
- Consider stepper motors with external drivers for extreme torque needs

---

## 4. Purchase Links (Verified)

- **DS3218 (20–21.5 kg·cm):**  
  [Amazon DS3218](https://www.amazon.com/DS3218-Torque-Digital-Waterproof-Rotation/dp/B07FMBBPD2)

- **LewanSoul LX-224HV (20 kg·cm):**  
  [Amazon LX-224HV](https://www.amazon.com/LewanSoul-Connectors-Equipped-Position-Temperature/dp/B081CTX6DM)

- **MG996R (11 kg·cm):**  
  [Amazon MG996R](https://www.amazon.com/MG996R-Digital-Torque-Metal-Gear/dp/B00KKTR0TY)

---

## 5. Suggested Project Structure on GitHub

