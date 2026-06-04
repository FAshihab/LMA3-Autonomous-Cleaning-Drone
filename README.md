# LMA3: AI-Powered Autonomous Window Cleaning Drone Using Webots Simulation

An open-source robotics project featuring **LMA3**, an autonomous quadcopter drone simulation engineered to revolutionize high-rise building maintenance. Developed for the *ARTI407 - Robotics and Intelligent Systems* course, this system replaces dangerous manual window cleaning with an automated, sensor-driven cleaning and flight-control architecture.

---

## Problem Statement & Objectives
* **The Challenge:** Manually cleaning the glass facades of tall buildings exposes workers to high safety risks, consumes significant time and labor, and imposes massive operational costs. 
* **Our Solution:** To design and build a simulated autonomous drone that safely and efficiently scans window surfaces, detects target areas, and performs automated cleaning maneuvers with minimal human intervention.

---

## System Architecture & Workflow
The drone operates within the **Webots Simulation Environment** and executes its workflow in four major operational phases:

1. **Phase 1 (Surface Scanning):** The drone initiates a stable flight path using its onboard camera to scan the building's windows.
2. **Phase 2 (Targeted Cleaning):** Upon locating dirt spots, the drone maintains a constant, safe distance from the window surface using a real-time laser distance measuring sensor and GPS coordinates.
3. **Phase 3 (Secondary Scan):** The system continuously rescans the window while executing the cleaning pattern to ensure thorough surface maintenance.
4. **Phase 4 (Model Retraining):** Generated clean/dirty window images are collected to feed into a Convolutional Neural Network (CNN) model via EfficientNet for continuous system retraining and optimization.

---

## Hardware & Software Integration
The simulation integrates continuous real-time sensor processing and flight control mechanisms:

* **Hardware Components (Simulated):** Quadcopter Drone body, GPS Sensor (Virtual), Gyroscope, Laser Distance Measuring Sensor, 4x Propeller Motors, Flight Controller, and Camera.
* **Core Motion Control Features:**
  * Altitude stabilization utilizing automated thrust control.
  * Smooth turning and orientation adjustments via Yaw calculations.
  * Pitch adjustments for precise movement balancing.
  * Radial and coordinate corrections to ensure a fixed distance from the structure.

---

## Technical Challenges & Implemented Solutions
* **Directional Instability:** Solved by developing custom yaw adjustment calculations to stabilize the drone's flight vector.
* **Tool Constraints in Webots:** Overcame the lack of native wiping utilities by engineering a custom Python cleaning function that activates to erase dirt spots as soon as the drone reaches target coordinates.
* **Drone Drifting Anomalies:** Rectified position drift by turning and optimizing specific layout and movement parameters (`RADIUS_X` and `RADIUS_Y`), dynamically drawing the drone closer and parallel to the building facade during execution.

---

## Tech Stack & Environment
* **Simulation Software:** Webots Simulation Environment
* **Programming Language:** Python
* **Core Libraries:** `NumPy` for operational matrix calculations, `EfficientNet` (CNN structure for visual analysis).
* **System Capabilities:** Real-time sensor parsing, autonomous path correction, and control algorithms.

* ## Authors & Affiliation
* **Abrar Almutawa**
* **Sara Alidrissi**
* **Zahra Alrowaei**
* **Jana Alhumaidan**
* **Tayma Aldobas**
* **Fatimah Al Shihab**

*College of Computer Science and Information Technology, Imam Abdulrahman Bin Faisal University (IAU), Dammam, Saudi Arabia.*  
