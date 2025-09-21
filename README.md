

# 🌿 VAYURAKSHAK
### AI-Powered Autonomous Drone  
*Precision Weed Management System using AI and Computer Vision*

---

## 📚 Table of Contents
- [Key Features](#-key-features)
- [Problem Statement](#-problem-statement)
- [Our Solution](#-our-solution)
- [System Architecture](#-system-architecture)
- [Technical Innovation](#-technical-innovation)
- [Expected Impact](#-expected-impact)
- [Team Members](#-team-members)
- [Future Scope](#-future-scope)
- [Installation](#-installation)
- [Usage](#-usage)
- [Contact](#-contact)

---

## ✨ Key Features  
- ✅ *Real-time weed detection*  
- ✅ *GPS mapping*  
- ✅ *Precision spraying (80–90% herbicide reduction)*  
- ✅ *5× faster than manual labor*  
- ✅ *Reaches any terrain*  
- ✅ *Generates weed maps for future planning*

```bash
pip install vayurakshak


---

## 🎯 Problem Statement

⚠ Key Challenges

Labor Intensity: 50–60 labor days per acre.

Inefficient Spraying: Traditional methods waste 70%+ of herbicides.

Environmental Harm: Chemical runoff, pollution, and contamination of nearby water sources.

Accessibility Issues: Large machinery cannot access uneven, terraced, or rocky terrain.



---

💡 Our Solution

An autonomous quadcopter system designed for precision weed management:

👁 Sees: High-resolution camera scans the field in real-time.

🗺 Maps: On-device AI detects weeds and geotags them via GPS.

💦 Sprays: Micro-droplet nozzles deliver herbicide only to detected weeds, drastically reducing usage.


Key outcomes: minimal human supervision, reduced chemical usage, faster operations, and precise weed maps for planning.


---

🛠 System Architecture

1. Field Monitoring

High-res camera or drone-mounted imaging system captures field images or video.



2. Navigation

GPS-based flight planning and waypoint navigation for full field coverage.



3. Core Controller

Raspberry Pi (or equivalent SBC) running the control loop and TensorFlow Lite models.



4. AI Vision

CNN model for weed vs. crop classification running on edge (TFLite).



5. GPS Mapping

Each detection is geotagged and stored for later visualization (weed density maps).



6. Action Command

Real-time command module triggers micro-sprayers when the drone is over a detected weed.



7. Precision Spray

Micro-droplet nozzles that spray small targeted bursts to minimize herbicide.



8. Data Analytics

Optional cloud upload for dashboard visualization, trend analysis, and record keeping.





---

🔬 Technical Innovation

🚀 Edge-AI on Raspberry Pi: Run optimized TFLite models on-board for low-latency inference.

💦 Custom Micro-Spraying: Hardware-level nozzle control for spot-spraying weeds only.

📍 Automated Geotagging: Generate accurate weed maps for future planning and variable-rate application.

🤖 End-to-End Automation: From image capture → detection → spray actuation → mapping with minimal human input.

💰 Cost-Effective Design: Built using affordable components to keep the solution accessible to smallholder farmers.



---

📊 Expected Impact

💰 Economic

Up to 80% reduction in weeding labor costs.

Up to 90% reduction in herbicide usage compared to conventional blanket spraying.


🌱 Environmental

Reduced chemical runoff and lower environmental contamination.

Supports sustainable agriculture and healthier soils.


👥 Social

Reduces repetitive labor burden.

Creates new rural technical jobs (drone operators, maintenance, data analysts).



---

👥 Team Members

Salma Kousar

Vaishnavi Chauhan

Mohammed Junaid Ahmed

Mohammed Junaid Ahmed


Problem Statement Code: SHH25097


---

🚀 Future Scope

Integrate with farm management software (FMS) and precision agriculture platforms.

Multi-drone swarming for faster coverage of large farms.

Support for organic herbicide or biological controls.

Expand vision models to detect pests, nutrient deficiency, and irrigation issues.

Add variable-rate application capability based on weed density maps.



---

⚙ Installation

Prerequisites (example):

Raspberry Pi 4 or similar SBC

Drone/flight controller compatible with companion computer (e.g., ArduPilot or PX4)

Camera module (Raspberry Pi camera or higher-res USB camera)

GPS module

Micro-sprayer hardware + solenoid valves

Python 3.8+

TensorFlow Lite runtime


Install Python package (if published):

pip install vayurakshak
---

▶ Usage (high-level)

1. Train or use a pre-trained TFLite weed-detection model.


2. Upload the model to the Raspberry Pi (or onboard device).


3. Calibrate the drone camera and GPS.


4. Configure flight waypoints and spray parameters.


5. Run the main control script to start field scanning, detection, and precision spraying.



Example command (script name may vary):

python main.py --mode auto --model models/weed_detector.tflite --waypoints wp.json


---

📁 File Structure (example)

vayurakshak/
├─ models/
│  └─ weed_detector.tflite
├─ scripts/
│  ├─ main.py
│  ├─ navigation.py
│  └─ sprayer_control.py
├─ config/
│  └─ wp.json
├─ data/
│  └─ detections.csv
├─ README.md
└─ requirements.txt


---

🧾 Notes & Safety

Test in a controlled environment before field deployment.

Follow local regulations for drone flights and pesticide usage.

Ensure herbicides used are approved and applied according to label instructions.

Implement emergency stop and fail-safe behaviors in navigation and spraying modules.

