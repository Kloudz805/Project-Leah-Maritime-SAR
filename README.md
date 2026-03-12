# 🌊 Project Leah-SAR: Maritime & Gemini RX Preset
![Betaflight](https://img.shields.io/badge/Betaflight-4.4%2B-blue) ![License](https://img.shields.io/badge/License-MIT-green)

> *High-reliability Betaflight presets optimized for maritime FPV Search & Rescue, featuring Gemini RX multipathing mitigation and over-water signal stability.*

## 🌍 The Mission
Flying over open water presents unique RF challenges, primarily severe signal multipathing caused by water reflections. This branch of **Project Leah-SAR** is dedicated to coastal and maritime operations, ensuring that drones deployed over water maintain a rock-solid control link and clear video feed, even in high-interference coastal zones.

## ✨ Key Features
* **📶 Gemini RX Optimization:** Specifically tuned to take advantage of dual-antenna True Diversity (Gemini) receivers to aggressively filter out water-bounce multipathing.
* **🌬️ Coastal Wind Resilience:** Filter and PID adjustments designed to handle sustained coastal crosswinds without oscillating the video feed.
* **👁️ Visual Clarity:** VTX and camera baseline settings geared toward cutting through water glare and haze to improve victim detection.
* **💧 Conformal-Ready:** Acknowledges the necessity of waterproofing and accounts for slightly higher operating temperatures in sealed builds.

## ⚙️ Quickstart Installation
Copy and paste the following snippet directly into your Betaflight CLI. *(Note: Ensure you are on Betaflight 4.4+ and utilizing ELRS Gemini/True Diversity hardware).*

```text
# Project Leah-SAR: Maritime & Gemini RX Base Preset
# Author: Kloudz805

# Link Quality & Multipath Mitigation (Assumes Gemini Hardware)
set crsf_telemetry_ratio = 7
set vtx_low_power_disarm = ON

# Coastal Wind Filtering
set dterm_lowpass_hz = 70
set gyro_lowpass_hz = 85

# Low-Resource Blackbox Logging
set blackbox_p_ratio = 64
set blackbox_mode = NORMAL

save

 ```
🛠️ Recommended Hardware
​Maritime operations require specialized preparation. Best results are achieved using:
​Receivers: True Diversity / Gemini RX (e.g., BetaFPV SuperD, Radiomaster Bandit).
​Protection: 100% Conformal Coating on all FC, ESC, and VTX components.
​High-Output VTX: Capable of pushing maximum legal output power to punch through coastal haze.
​🗺️ Roadmap
​[x] Gemini RX baseline signal optimization
​[ ] High-wind PID adjustments for 7" frames
​[ ] Integration with Project Exocoetus maritime AI-vision detection
​[ ] Telemetry recovery protocols for water-ditching scenarios
​⭐️ Support the Project!
​If this maritime preset helped you maintain a vital link over water, please consider hitting the Star button at the top right of this repository. It helps push this tool up in the algorithm so it reaches the coastal operators who need it most!
​Built to save lives. 🇺🇦
