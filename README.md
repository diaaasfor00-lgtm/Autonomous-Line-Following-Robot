# Autonomous Line-Following Robot


https://github.com/user-attachments/assets/d7f5bbb0-5e21-4ff6-80e8-383300a92aa8


An autonomous two-wheel-drive (2WD) line-following robot engineered using an **Arduino Uno**, an **L298N Dual H-Bridge motor driver**, and a front-mounted **IR reflectance sensor array** to track closed-loop paths, sharp curves, and track intersections.

## Hardware Architecture

- **Microcontroller:** Arduino Uno (ATmega328P)
- **Motor Driver:** L298N Dual H-Bridge DC Motor Driver (PWM speed & direction control)
- **Sensors:** Multi-channel Infrared (IR) Line-Tracking Sensor Array
- **Actuators:** Dual DC Geared Motors + Front Caster Wheel
- **Power Supply:** Dual 18650 Li-ion Battery Pack

## Hardware Setup
<img width="1536" height="2048" alt="PHOTO-2024-12-30-19-56-54" src="https://github.com/user-attachments/assets/e88b54e9-2993-4b27-808c-6a0c54dccd72" />

## Key Engineering Highlights
- **Closed-Loop Path Tracking:** Continuously reads digital/analog reflectance states from the front IR array to compute steering corrections in real time.
- **Differential Drive Control:** Modulates left and right wheel speeds independently via PWM signals (`ENA`/`ENB`) through the L298N driver to handle tight corners smoothly without overshooting.
- **Power & Signal Isolation:** Structured wiring separation between the Li-ion motor power rail and the microcontroller logic lines to prevent voltage drops and sensor noise.

## Live Track Demonstration
Watch the robot navigating curved segments and track junctions autonomously:
