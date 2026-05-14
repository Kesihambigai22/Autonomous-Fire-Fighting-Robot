#  Software Implementation

This folder contains the Arduino code for the Autonomous Fire Fighting Robot.

---

#  Files Included

| File | Description |
|---|---|
| main_code.ino | Main Arduino program |
| README.md | Software documentation |

---

#  Software Features

The software controls:
- Fire detection
- Obstacle avoidance
- Motor navigation
- Servo movement
- Water pump activation

---

#  Software Workflow

```text
Start Robot
     ↓
Read Ultrasonic Sensor
     ↓
Avoid Obstacles
     ↓
Check Flame Sensor
     ↓
Fire Detected?
   ↙       ↘
 YES       NO
  ↓         ↓
Stop      Continue
Robot     Navigation
  ↓
Rotate Servo
  ↓
Activate Pump
  ↓
Extinguish Fire
