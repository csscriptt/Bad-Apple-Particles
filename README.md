# 🍎 Bad Apple!! Zero-Skip Fluid Particles

An interactive, high-performance particle engine that reconstructs the iconic **Bad Apple!!** music video in real-time. By combining fluid mechanics visuals with real-time FFmpeg audio stream analysis, this project creates a high-fidelity visualizer where thousands of particles react dynamically to the animation track.

## 🚀 Key Features

* **Zero-Skip Synchronization:** Uses a raw, low-overhead FFmpeg audio pipeline engine to stream audio samples instantly.
* **Audio Energy Analysis:** Real-time calculation of audio frequencies to dynamically scale and impact fluid particles.
* **Hardware-Accelerated Visuals:** Leverages Pygame's hardware surfaces and double-buffering for fluid, high-frame-rate particle trailing.
* **Responsive Control:** Instant fullscreen toggle (`F` or `F11`) with automated aspect-ratio fitting.

---

## 📥 How to Download & Set Up

### 🪟 Windows Setup

#### 1. Download the Code
Open PowerShell and clone the repository:
```bash
git clone https://github.com
cd Bad-Apple-Particles
```

#### 2. Install Dependencies
Run the following command to download the modern package environment requirements:
```bash
pip install opencv-python numpy sounddevice pygame-ce
```
*(Note: We use `pygame-ce` because legacy pygame fails to build from source on modern Python versions).*

#### 3. Install FFmpeg via Terminal
In your PowerShell window, install FFmpeg instantly via the Windows Package Manager:
```bash
winget install Gyan.FFmpeg
```
**Important:** Once the installation finishes, close your current PowerShell window entirely and open a brand-new one to refresh your system's PATH variables.

#### 4. Run the Project
Navigate back to your folder, drop your video file inside it, rename the video to `bad_apple_new.mp4`, and run:
```bash
cd Bad-Apple-Particles
python Bad_Apple_Particles
```
Place your video file inside the folder, name it `bad_apple_new.mp4`, and run:
```bash
python Bad_Apple_Particles
```

---

### 🐧 Linux Setup (Ubuntu / Debian / Mint)

#### 1. Download the Code & Install Dependencies
Open your terminal and run:
```bash
git clone https://github.com/csscriptt/Bad-Apple-Particles          
cd Bad-Apple-Particles
sudo apt update
sudo apt install python3 python3-pip python3-venv ffmpeg libasound2-dev libportaudio2 -y
```

#### 2. Set Up Environment & Run
```bash
python3 -m venv venv
source venv/bin/activate
pip install opencv-python numpy sounddevice pygame
```
Place your video file inside the folder, name it `bad_apple_new.mp4`, and run:
```bash
python Bad_Apple_Particles
```

---

### 🎩 Linux Setup (Fedora)

#### 1. Download the Code & Install Dependencies
Open your terminal and run:
```bash
git clone https://github.com/csscriptt/Bad-Apple-Particles          
cd Bad-Apple-Particles
sudo dnf install fedora-workstation-repositories
sudo dnf config-manager --set-enabled rpmfusion-free
sudo dnf install ffmpeg python3 python3-pip portaudio-devel -y
```

#### 2. Set Up Environment & Run
```bash
python3 -m venv venv
source venv/bin/activate
pip install opencv-python numpy sounddevice pygame
```
Place your video file inside the folder, name it `bad_apple_new.mp4`, and run:
```bash
python Bad_Apple_Particles
```

---

## 🛠️ Troubleshooting

* **Missing Video Error:** If you get `Could not find the file 'bad_apple_new.mp4'`, verify the exact file name and make sure it sits in the same directory where your terminal is currently running.
* **FFmpeg Command Not Found:** If Windows crashes with a `WinError 2`, your system path variables are incorrect. Restart your terminal or computer after configuring FFmpeg.
* **PortAudio Error:** If `sounddevice` fails, ensure your host has a working, unmuted audio output device plugged in. On Linux, ensure your user belongs to the audio group: `sudo usermod -aG audio $USER`.
