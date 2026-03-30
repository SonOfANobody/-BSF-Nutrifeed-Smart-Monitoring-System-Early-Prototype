## BSF Nutrifeed Monitor: AI Larvae Surveillance 📡

An automated Computer Vision system designed to monitor the population health and density of Black Soldier Fly (BSF) larvae in real-time. This project helps farmers move from manual inspections to data-driven insect farming. 🚜✨

## 🌟 Key Features

🔍 Real-Time Detection: Uses HSV color segmentation to identify larvae clusters.

📊 Automatic Logging: Records population counts and timestamps every 5 seconds into a bsf_monitor_log.csv.

🩺 Health Classification: Automatically labels the tray status:

🟢 Healthy Growth: 5+ Larvae (Optimal density)

🟡 Low Density: 2-4 Larvae (Action recommended)

🔴 Possible Contamination: 0-1 Larvae (Critical alert)

🚨 Smart Alert System: Triggers a visual alarm if zero activity is detected for more than 10 seconds.

📸 Evidence Snapshots: Automatically saves a .jpg photo when a critical alert occurs for later review.

📈 Data Visualization: Includes a script to turn CSV logs into professional growth charts.

## 🛠️ Technology Stack

Python 3.x 🐍

OpenCV: Image processing and contour detection.

NumPy: Mathematical array handling.

Matplotlib / Pandas: Data analysis and visualization.

Time / CSV / OS: System-level logging and file management.

## 🚀 Installation & Setup

Clone the repository:

Bash

git clone https://github.com/sonofanobody/bsf-nutrifeed-smart-monitoring-system-early-protoype.git

cd bsf-monitor

Install Dependencies:

Bash

pip install opencv-python numpy pandas matplotlib python-pptx

Run the Monitor:

Bash

python main_monitor.py

Generate the Growth Chart:

Bash

python visualize_data.py

📂 Project Structure

Plaintext

├── alerts/               # 📸 Folder where alert snapshots are saved

├── bsf_monitor_log.csv   # 📄 Historical data log (Auto-generated)

├── main_monitor.py       # 🧠 The core CV tracking script

├── visualize_data.py     # 📈 Script to generate growth graphs

└── README.md             # 📖 This file!

## 🧠 Challenges & Solutions

Issue: Variable lighting made larvae hard to see. 💡

Fix: Switched to HSV Color Space to isolate the larvae's specific pigment regardless of shadows.

Issue: Constant "False Alarms" from the camera flickering. ⚠️

Fix: Implemented a 10-second Time-Buffer before triggering the contamination alert.

## 🤝 Acknowledgement 

Developed for the AgTech Innovation Track - 2026 🚀
