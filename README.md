```markdown
# 🚦 AI Vehicles & Traffic Signal Detection System (Ubuntu Based)

[![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-2.3.3-black?style=for-the-badge&logo=flask)](https://flask.palletsprojects.com/)
[![YOLOv8](https://img.shields.io/badge/YOLOv8-Object%20Detection-orange?style=for-the-badge&logo=ultralytics)](https://ultralytics.com/)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-22.04+-E95420?style=for-the-badge&logo=ubuntu)](https://ubuntu.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

An **AI-powered real-time traffic environment detection system** that identifies vehicles (car, bike, bus, truck) and traffic signals using a **live camera feed**.  
The system can operate in both **manual** and **autonomous drive modes**, communicating with an **Arduino-based robot car** to make smart movement decisions.


assets/demo.gif

```

![Dashboard Preview](assets/screenshot.png)

---

## ✨ Features

| Feature | Details |
|--------|---------|
| 🚘 Vehicle Detection | Detects cars, bikes, buses, trucks in real-time. |
| 🚦 Traffic Signal Detection | Identifies Red / Yellow / Green signals from camera input. |
| 📡 Live Streaming | View camera feed directly in the web dashboard. |
| 🎮 Manual Control Mode | Control the robot car (Forward, Back, Turn Left/Right). |
| 🤖 Autonomous Driving Mode | System automatically slows/stops the car based on obstacles & signals. |
| 🔌 Arduino Communication | Uses **PySerial** to send movement commands to the car. |
| 🎛 OLED Display Simulation | Shows state feedback such as speed, mode, and alerts. |

---

## 🧱 Tech Stack

| Layer | Technology |
|------|------------|
| **AI Model** | YOLOv8 |
| **Backend** | Flask (Python) |
| **Video Processing** | OpenCV |
| **Robot Hardware** | Arduino + Motor Driver |
| **Frontend** | HTML, CSS, JavaScript |

---

## 📂 Project Structure

```

AI-Vehicles-Detection-System-traffic-signals-detection/
├── app.py
├── requirements.txt
├── README.md
├── models/
│   ├── best.pt
│   └── last.pt
├── templates/
│   ├── index.html
│   └── live.html
├── assets/
│   ├── screenshot.png
│   └── demo.gif
└── arduino/
└── update_car/
└── update_car.ino

````

---

## 🛠️ Installation (Ubuntu)

### 1️⃣ Install System Tools
```bash
sudo apt update
sudo apt install python3-pip python3-venv git
````

### 2️⃣ Allow Camera Access

```bash
sudo usermod -a -G video $USER
```

Logout & login again.

### 3️⃣ Clone Project

```bash
git clone https://github.com/Shahzadabbas28/AI-Vehicles-Detection-System-traffic-signals-detection.git
cd AI-Vehicles-Detection-System-traffic-signals-detection
```

### 4️⃣ Create Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### 5️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 6️⃣ Configure Model + Arduino Port

Find Arduino port:

```bash
ls /dev/ttyACM*
```

Edit in `app.py`:

```python
MODEL_PATH = './models/best.pt'
ARDUINO_PORT = '/dev/ttyACM0'
```

### 7️⃣ Run Application

```bash
python app.py
```

Open in browser:

```
http://localhost:5000
```

---

## 🎮 Usage

| Page    | Function                                          |
| ------- | ------------------------------------------------- |
| `/`     | Upload image/video for detection                  |
| `/live` | Live camera detection + manual & auto car control |

**Autonomous mode automatically:**

* Stops at **Red** signal
* Slows when vehicle is **too close**
* Turns or stops based on obstacle detection

---

## 🤝 Contributing

Contributions are welcome. Fork the repo → create a branch → submit PR.

---

## 📜 License

Distributed under the **MIT License**. See **LICENSE** for details.

---

## 📬 Contact

| Method      | Details                                                                                                                                                                              |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| WhatsApp    | +92 300 5704178                                                                                                                                                                      |
| Email       | [shahzadabbas4178@gmail.com](mailto:shahzadabbas4178@gmail.com)                                                                                                                      |
| GitHub Repo | [https://github.com/Shahzadabbas28/AI-Vehicles-Detection-System-traffic-signals-detection](https://github.com/Shahzadabbas28/AI-Vehicles-Detection-System-traffic-signals-detection) |

---

⭐ **If you like this project, please give it a star on GitHub — it motivates further updates!**
