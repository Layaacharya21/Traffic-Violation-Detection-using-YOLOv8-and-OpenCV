# Real-Time Traffic Violation Detection System

A high-performance computer vision solution utilizing **YOLOv8**, **OpenCV**, and **EasyOCR** to automate road safety enforcement through real-time violation detection and **Automatic Number Plate Recognition (ANPR)**.

---

## Project Overview
Road accidents and fatalities are frequently caused by traffic violations like riding without helmets or driving without seatbelts. This project addresses these critical challenges by establishing a real-time monitoring and enforcement system.

The system identifies non-compliant behavior and automatically extracts vehicle license plates to facilitate law enforcement. It is designed to be adaptable for **Smart City** initiatives and traffic safety improvement purposes.

---

## Key Features
* **Advanced Object Detection:** Uses the **YOLOv8** model to detect motorcycle riders without helmets and car occupants without seatbelts.
* **Automated ANPR:** Employs **Automatic Number Plate Recognition** to identify and log vehicle license plates for enforcement.
* **Optimized Image Processing:** Implements **OpenCV** techniques such as:
    * **Frame Skip:** Ensures optimal frame capture for real-time processing.
    * **Adaptive Thresholding:** Enhances number plate visibility in diverse lighting and weather conditions.
* **High-Precision OCR:** Integrates **EasyOCR** for robust text extraction from localized license plates.
* **Real-Time Dashboard:** Features a user-friendly **Streamlit** interface to display detections, plate numbers, and confidence metrics.

---

## Technical Architecture



The system operates through a structured multi-stage pipeline:

1.  **Preprocessing:** Frames are optimized using frame-skipping and adaptive thresholding via OpenCV.
2.  **Violation Detection:** YOLOv8 identifies vehicles and checks for the presence of helmets or seatbelts.
3.  **Plate Localization:** If a violation is detected, the system crops the vehicle's license plate region.
4.  **Text Extraction:** EasyOCR converts the visual license plate into digital text.
5.  **Visualization:** Data is streamed to a Streamlit interface for human verification and logging.

---

## Performance & Validation
* **Precision & Recall:** The system accurately detects violations with high metrics across varying conditions.
* **Environmental Robustness:** Performance has been validated in alternative capturing conditions, including different light levels and weather patterns.
* **Scalability:** The architecture is designed for easy integration into existing smart city infrastructure.

---

## Tech Stack
* **Deep Learning:** YOLOv8
* **Image Processing:** OpenCV
* **OCR Engine:** EasyOCR
* **UI/Frontend:** Streamlit
* **Language:** Python

---

## Getting Started

### Prerequisites
* Python 3.9+
* NVIDIA GPU (Recommended for real-time performance)

### Installation
```bash
# Clone this repository
git clone [https://github.com/your-username/traffic-violation-detection.git](https://github.com/your-username/traffic-violation-detection.git)

# Install dependencies
pip install ultralytics opencv-python easyocr streamlit
