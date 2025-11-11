
```markdown
# 🚗 AI-Powered Vehicle Detection and Traffic Signal detection System for Ubuntu

[![Python Version](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![Flask Version](https://img.shields.io/badge/Flask-2.3.3-green?style=for-the-badge&logo=flask)](https://flask.palletsprojects.com/)
[![YOLOv8](https://img.shields.io/badge/YOLOv8-8.1.25-FFA500?style=for-the-badge&logo=ultralytics)](https://ultralytics.com/)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-22.04%2B-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)](https://ubuntu.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](https://opensource.org/licenses/MIT)

An intelligent, real-time object detection system for an automated car, optimized for **Ubuntu**. This project leverages the power of **YOLOv8**, **Flask**, and **Arduino** to create a smart vehicle that can autonomously detect cars, bikes, trucks, and traffic signals from a live camera feed, and react to its environment.

---

## 🎬 Demo

*See the system in action! Detecting vehicles and controlling the car in real-time.*

> **Tip:** Replace the placeholder image below with your own GIF or video for maximum impact!
> `![Demo GIF](assets/demo.gif)`

![Main Dashboard Screenshot](assets/screenshot.png)

---

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| 🚗 **Real-Time Detection** | Live object detection from a camera feed using the state-of-the-art YOLOv8 model. |
| 📁 **File Analysis** | Upload images or videos for on-demand object detection and analysis. |
| 🕹️ **Manual Control** | Take full control with a web-based interface to drive the car (forward, turn, stop). |
| 🤖 **Autonomous Mode** | Toggle an intelligent mode that automatically stops and turns the car to avoid obstacles. |
| 📺 **OLED Display Sim** | A real-time simulation of an OLED display showing vital stats and car status. |
| 🔌 **Arduino Integration** | Seamless communication with an Arduino to control the car's physical motors. |
| 📏 **Distance Estimation** | Calculates the distance of detected objects for smarter autonomous decisions. |

---

## 🛠️ Technology Stack

This project is built with a combination of powerful open-source technologies.

*   **Backend**: `Flask` (Python Web Framework)
*   **Computer Vision**: `YOLOv8` (Object Detection Model), `OpenCV` (Image Processing)
*   **Hardware Control**: `PySerial` (Arduino Communication)
*   **Frontend**: `HTML5`, `CSS3`, `JavaScript`

---

## 📁 Project Structure

A clean and organized layout for easy development and contribution.

```
Automated-Car-Detection-System/
├── .gitignore
├── README.md
├── requirements.txt
├── app.py
├── assets/
│   ├── demo.gif
│   └── screenshot.png
├── templates/
│   ├── index.html
│   └── live.html
├── models/
│   ├── best.pt
│   └── last.pt
└── arduino/
    └── update_car/
        └── update_car.ino
```

---

## 🚀 Getting Started on Ubuntu

Follow these simple steps to get a copy of the project up and running on your Ubuntu machine.

### 1. Install System Dependencies

First, open a terminal (`Ctrl+Alt+T`) and install Python and pip, along with other essential tools.

```bash
sudo apt update
sudo apt install python3-pip python3-venv git
```

### 2. Grant Camera Permissions (Important!)

To allow the application to access your USB camera, add your user to the `video` group. You will need to log out and log back in for this to take effect.

```bash
sudo usermod -a -G video $USER
```

### 3. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Automated-Car-Detection-System.git
cd Automated-Car-Detection-System
```

### 4. Set Up a Virtual Environment

Using a virtual environment isolates project dependencies and is a best practice.

```bash
# Create a virtual environment
python3 -m venv venv

# Activate it
source venv/bin/activate
```
*Your terminal prompt should now start with `(venv)`.*

### 5. Install Python Dependencies

Install all the necessary Python packages from the `requirements.txt` file.

```bash
pip install -r requirements.txt
```

### 6. Configure Hardware & Software

1.  **Place Model Files**: Add your pre-trained `best.pt` and `last.pt` files into the `models/` directory.
2.  **Find Your Arduino Port**: Connect your Arduino and run this command to find its serial port.
    ```bash
    ls /dev/ttyACM*
    ```
    The output is likely `/dev/ttyACM0`. If not, use the port that appears.
3.  **Update Paths in `app.py`**: Open `app.py` with a text editor (like `nano` or `gedit`) and modify the following variables.
    ```bash
    nano app.py
    ```
    ```python
    # Example: Update this path to where your model is located
    MODEL_PATH = '/home/youruser/Automated-Car-Detection-System/models/best.pt'

    # Update this to the Arduino port you found in the previous step
    ARDUINO_PORT = '/dev/ttyACM0'
    ```

### 7. Run the Application

Launch the Flask server.

```bash
python app.py
```

Now, open your web browser and navigate to **`http://localhost:5000`**.

---

## 🎮 How to Use

1.  **File Upload (`/`)**: Upload an image or video to get static detection results.
2.  **Live Detection (`/live`)**:
    *   Click **"Start Camera"** to begin the real-time video stream.
    *   Use the **Manual Control** buttons to drive the car yourself.
    *   Toggle **"Autonomous Mode"** to enable smart obstacle avoidance.

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

---

## 📝 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

## 📧 Contact

Whatsapp: +92300-5704178
Email - shahzadabbas4178@gmail.com


Project Link: https://github.com/Shahzadabbas28/AI-Vehicles-Detection-System-traffic-signals-detection
```
