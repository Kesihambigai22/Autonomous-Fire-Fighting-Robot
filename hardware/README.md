# Hardware Setup – Autonomous Fire Fighting Robot

This folder contains the hardware implementation and circuit design of the Autonomous Fire Fighting Robot project.

---

# Hardware Components

| Component | Quantity | Purpose |
|---|---|---|
| Arduino Uno | 1 | Main microcontroller |
| Flame Sensor | 1 | Detects fire |
| Ultrasonic Sensor HC-SR04 | 1 | Obstacle detection |
| L298N Motor Driver | 1 | Controls DC motors |
| DC Motors | 2 | Robot movement |
| Servo Motor | 1 | Rotates water nozzle |
| Mini Water Pump | 1 | Sprays water |
| Wheels | 2 | Robot mobility |
| Robot Chassis | 1 | Mechanical structure |
| Battery Pack | 1 | Power supply |
| Jumper Wires | Multiple | Circuit connections |
| Breadboard | 1 | Prototyping |

- Arduino Uno (Microcontroller)
- Flame Sensor (Fire detection)
- Ultrasonic Sensor HC-SR04 (Obstacle avoidance)
- L298N Motor Driver
- DC Motors with wheels
- Servo Motor
- Water Pump
- Battery (7.4V–12V)
---

# Power Requirements

| Device | Voltage |
|---|---|
| Arduino Uno | 5V |
| L298N Motor Driver | 7V–12V |
| DC Motors | 6V–12V |
| Servo Motor | 5V |
| Water Pump | 5V–12V |
| Sensors | 5V |

---

# Pin Connections

---

# Flame Sensor → Arduino

| Flame Sensor | Arduino |
|---|---|
| VCC | 5V |
| GND | GND |
| OUT | Digital Pin 7 |

### Function
Detects fire/flame and sends signal to Arduino.

---

# Ultrasonic Sensor HC-SR04 → Arduino

| HC-SR04 | Arduino |
|---|---|
| VCC | 5V |
| GND | GND |
| TRIG | Pin 9 |
| ECHO | Pin 10 |

### Function
Measures distance for obstacle avoidance.

---

# L298N Motor Driver → Arduino

| L298N | Arduino |
|---|---|
| ENA | Pin 5 |
| IN1 | Pin 2 |
| IN2 | Pin 3 |
| ENB | Pin 6 |
| IN3 | Pin 4 |
| IN4 | Pin 8 |

### Function
Controls direction and speed of DC motors.

---

# Servo Motor → Arduino

| Servo Pin | Arduino |
|---|---|
| VCC | 5V |
| GND | GND |
| Signal | Pin 11 |

### Function
Rotates nozzle toward fire source.

---

# Water Pump → Relay/L298N

| Pump Wire | Connection |
|---|---|
| Positive | Motor Driver Output |
| Negative | GND |

### Function
Sprays water to extinguish fire.

---

# Hardware Working Flow

```text
Flame Sensor
      ↓
Arduino Uno
      ↓
Obstacle Detection using Ultrasonic Sensor
      ↓
Motor Navigation
      ↓
Servo Alignment
      ↓
Water Pump Activation
      ↓
Fire Extinguished
