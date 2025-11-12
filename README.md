# Color-Blindness Support and Enhancement Service

## Overview
This project aims to develop an **AI-based assistive system for people with color vision deficiency (CVD)**.  
The service performs **real-time image analysis, color labeling, contrast enhancement, and accessibility evaluation**, allowing users to better recognize colors and interact with visual environments.

It integrates **machine learning (Keras / Teachable Machine)**, **computer vision (OpenCV)**, and **mobile accessibility (MIT App Inventor + Arduino)** to provide both **visual** and **haptic feedback**.

---

## Objectives
- Assist users with color blindness or color weakness (e.g., Deuteranopia, Protanopia, Tritanopia).  
- Identify confusing color regions in real time and enhance contrast or readability.  
- Provide **auditory (TTS)** and **vibration (motor)** feedback for quick recognition.  
- Offer accessibility scores and recommendations for UI designers or users.

---

## Core Features
| Feature | Description |
|----------|-------------|
| **Real-Time Color Detection** | AI model recognizes dominant colors from images, video, or live camera feeds. |
| **Contrast & Pattern Enhancement** | Improves distinguishability of confusing color pairs for CVD users. |
| **Text / Voice Labeling** | Displays or reads out color names (e.g., “This shirt is green”). |
| **Haptic Feedback** | Arduino vibration motor alerts users in critical color-based situations (e.g., red traffic lights). |
| **Accessibility Evaluation** | Calculates color contrast ratio and provides design recommendations. |

---

## System Architecture


**Modules**
1. **Segmentation (TensorFlow U-Net / DeepLab)**  
   - Identifies distinct objects or regions in the image.  
2. **Color Classification (Keras / Teachable Machine)**  
   - Predicts the perceived color category of each region.  
3. **Accessibility Scoring (OpenCV)**  
   - Measures WCAG contrast ratio and CVD confusion index.  
4. **Feedback Delivery**  
   - MIT App Inventor provides TTS or overlay labels.  
   - Arduino triggers vibration signals for specific color alerts.

---

## Technical Stack
| Category | Tools & Frameworks |
|-----------|--------------------|
| **AI / ML** | TensorFlow, Keras, Teachable Machine |
| **Computer Vision** | OpenCV, NumPy, Pillow |
| **Mobile Interface** | MIT App Inventor |
| **Hardware Integration** | Arduino (Nano / ESP32, HC-05 or BLE) |
| **Programming Languages** | Python, Java (MIT Blocks), C/C++ (Arduino) |
| **Environment** | Google Colab, Android device, Breadboard prototype |

---

## Workflow
1. **Data Preparation**  
   - Collect 10,000+ labeled samples of different colors and lighting conditions.  
   - Apply CVD simulation filters for Deuter/Protan/Tritan types.  

2. **Model Training**  
   - Train a CNN classifier using Teachable Machine / Keras.  
   - Export to `.h5` or `.tflite` format for app integration.  

3. **Segmentation and Color Analysis**  
   - Use TensorFlow segmentation (DeepLab / U-Net) to detect object regions.  
   - Apply color classifier to each region for label assignment.  

4. **Accessibility Scoring**  
   - Compute contrast ratio: `(L1 + 0.05) / (L2 + 0.05)` (WCAG 2.1 standard).  
   - Evaluate confusion risk between red–green, blue–purple, etc.  

5. **Feedback Integration**  
   - App overlays color labels or reads them aloud.  
   - Arduino vibrates when high-risk colors (e.g., red signals) appear.  

---

## Evaluation Metrics
| Metric | Description |
|---------|-------------|
| **Top-1 / Top-3 Accuracy** | Correctness of color recognition |
| **Contrast Improvement Ratio (CIR)** | Improvement in visual distinguishability |
| **Processing Latency** | Target < 1.5 seconds for real-time feedback |
| **User Feedback Score** | Subjective satisfaction and accessibility improvement |

---

## Limitations & Ethical Considerations
- Accuracy depends on **camera quality and lighting conditions**.  
- Avoid over-reliance on AI in critical safety scenarios (e.g., driving).  
- Respect **user privacy** when processing camera data.  
- Use results only as **assistive reference**, not medical diagnosis.

---

## Future Work
- On-device TensorFlow Lite inference for offline mode.  
- Automatic color contrast correction for UI design.  
- Personalized calibration for each user’s vision profile.  
- Integration with smart glasses or wearable devices.

---

## Team & Contribution
| Role | Responsibility |
|------|----------------|
| AI / Vision Developer | Model training, image segmentation, and OpenCV pipeline |
| App Developer | MIT App Inventor interface, TTS integration |
| Hardware Engineer | Arduino connection, vibration and sensor logic |
| Accessibility Research | CVD simulation, UX testing, ethical validation |

---

## Author
**Project Lead:** [Jian Yi]  
**Affiliation:** [Hanyang University / Intercollege]  
**Version:** 1.0  
**Environment:** TensorFlow 2.x / Keras / Python 3.12 / Arduino IDE  
**Platform:** Google Colab + MIT App Inventor + Arduino BLE

---

## License
This project is for **academic and research purposes only**.  
Redistribution or commercial use requires permission from the authors.
