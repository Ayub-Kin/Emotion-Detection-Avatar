# Privacy-Aware Emotion Detection Avatar

This repository contains the code, questionnaires, and experiment setup for the paper:  
**Privacy-Aware Emotion Detection Using Large Language Models for Social Robots**.

The system integrates multimodal emotion detection (facial + vocal tone) with large language model (LLM) dialogue generation in a privacy-aware, real-time framework.

---

## 🚀 Features
- Real-time multimodal emotion detection (facial expressions + vocal tone).
- Privacy mode with automatic anonymization of sensitive data.
- Integration with LLaMA (via Ollama) for local LLM dialogue generation.
- Emotionally expressive avatar with synchronized speech and visuals.
- Live dashboard for monitoring detected emotions and system performance.

---

## 🖥 Requirements
- **OS**: Ubuntu 22.04 LTS (tested)/ Windows 10+  
- **Python**: 3.10 or higher  
- **Hardware**:  
  - Minimum: 16 GB RAM, CPU with 8 cores  
  - Recommended: NVIDIA GPU with at least 8 GB VRAM (tested with RTX 4090)  

- **Dependencies**: Listed in `requirements.txt`  
  - OpenCV  
  - Vosk API  
  - FER  
  - Flask  
  - MongoDB  
  - eSpeak-NG  

---

## ⚙️ Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Ayub-Kin/Emotion-Detection-Avatar
   cd Emotion-Detection-Avatar
2. Creat a virtual Environment inside your project folder:
    ```bash
    python3.10+ -m venv venv
   
3. Install Python requirements:
   ```bash
   pip install -r requirements.txt

4. Install Vosk
  Use pip to install the Python wrapper:
    ```bash
    pip install vosk
  
    If you also need the speech model (English example):
      ```bash
      mkdir models
      cd models
      wget https://alphacephei.com/vosk/models/vosk-model-small-en-us-0.15.zip
      unzip vosk-model-small-en-us-0.15.zip
      mv vosk-model-small-en-us-0.15 en-us
      cd ..

    Now your backend can load the model from backend/models/en-us.

5. Install eSpeak NG

    eSpeak is not a pure Python package — you need the system binary plus a Python wrapper.

      (i) On Ubuntu/Debian:

          sudo apt-get install espeak-ng
          pip install py-espeak-ng

      (ii) On Windows (using Git Bash or PowerShell):

          Download eSpeak NG [binaries](https://github.com/espeak-ng/espeak-ng)
          Add the espeak-ng folder to your PATH.
          
          Install Python bindings:
          ```bash
          pip install py-espeak-ng
   
6. Install and run MongoDB (if not already installed).
   See: MongoDB installation guide https://www.mongodb.com/
   
7. Install Ollama
   https://ollama.com/library/llama3.2:latest
   
▶️ Running the System
1. Start the backend:
   ```bash
   python emotion_api.py
   
2. Start the frontend
   ```bash
   npm start
   
3. Open the Control Panel in your browser at:
   http://localhost:5000/
   
5. Launch the User Interface (participant view) from the Control Panel.

7. To enable/disable all toggle options click them in the Control Panel.
