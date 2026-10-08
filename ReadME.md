# Self-Balancing Robot From Scratch

> Wiping the stock firmware of the Elegoo Uno Tumbler kit to write custom balancing algorithms and learn robotics from the ground up.

![Current Progress Photos](./images/robot_photo.jpg)

## Objective
The goal of this project is to bypass the pre-written Elegoo libraries and code a self-balancing robot from scratch using the **Arduino (C++)** ecosystem. By doing this, I aim to master:
* **Sensor Fusion:** Reading raw data from the MPU6050 Accelerometer/Gyroscope and filtering it (Complementary or Kalman filter).
* **Control Theory:** Implementing and tuning a custom PID (Proportional-Integral-Derivative) loop to keep the robot upright.
* **Actuation:** Driving the DC motors with precise PWM signals based on PID outputs.

## Hardware Stack
* **Kit:** [Elegoo Tumble Robot Kit]([https://elegoo.com](https://www.elegoo.com/en-gb/blogs/arduino-projects/elegoo-tumbller-self-balancing-robot-car-tutorial?srsltid=AU7gw4VqSs-i76UU92Y7a3WvjvENuY9Lcs4N4Jtv3x0NYm5Q2gpXxZTW))
* **Microcontroller:** Arduino Uno (built into the Elegoo shield)
* **IMU (Inertial Measurement Unit):** MPU6050 (6-axis gyro/accelerometer)
* **Motors:** Dual DC motors with encoders

## The Roadmap & Learning Phases
Because this project is starting from absolute zero, development is broken down into progressive milestones:

### Phase 1: Hardware & Sensor Validation ⚙️
- [ ] Read raw Gyro and Accel data via I2C from the MPU6050.
- [ ] Convert raw data into readable tilt angles (pitch/roll).
- [ ] Implement a **Complementary Filter** to eliminate sensor noise and drift.
- [ ] Test basic motor actuation (Forward, Backward, Stop).

### Phase 2: Core Balancing Loop ⚖️
- [ ] Write the mathematical math for the **PID Controller**.
- [ ] Establish a stable timing loop (e.g., executing the control loop every 10ms consistently).
- [ ] Tie the filtered IMU angle to the PID input and the PID output to the motor speed.

### Phase 3: Tuning & Stability (The Hard Part) 🛠️
- [ ] Tune \(K_p\) (Proportional) to get the robot oscillating back and forth.
- [ ] Tune \(K_d\) (Derivative) to dampen the oscillations and stabilize it.
- [ ] Tune \(K_i\) (Integral) to eliminate steady-state error so it doesn't drift.

### Phase 4: Expansion 🚀
- [ ] Utilize motor encoders for better position control.
- [ ] Implement Bluetooth or IR remote control for steering.

## Setup & How to Explore
Since this is an active learning journey, the `src/` directory is organized by evolution.

1. **Clone the repo:**
   ```bash
   git clone https://github.com
   ```
2. **Current State:** Open the `src/` folder to view individual test sketches (e.g., `01_imu_test.ino`, `02_motor_test.ino`) as I build up to the final balancing script.

## Resources Used
* *[Insert links to articles, YouTube channels, or papers on PID loops and MPU6050 filters that you are using to learn]*

## Contact
Your Name – email@example.com
