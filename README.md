# Wav2Lip: Accurately Lip-syncing Videos In The Wild

Welcome to the Wav2Lip project! This repository contains the complete setup guide and instructions to use Wav2Lip, a model that can lip-sync videos to any target speech with high accuracy. The model works for any identity, voice, and language, and is based on the research paper: "A Lip Sync Expert Is All You Need for Speech to Lip Generation In The Wild", published at ACM Multimedia 2020.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.6
- FFmpeg (Install using `sudo apt-get install ffmpeg` for Linux)

## Installation

Follow these steps to set up the Wav2Lip project:

1. **Clone the Repository:**
```
git clone https://github.com/Rudrabha/Wav2Lip.git
cd Wav2Lip
```

2. **Environment Setup:**
- **For MacOS:**
  ```
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  brew install pyenv
  mkdir Wav2LipProject && cd Wav2LipProject
  pyenv install 3.6.15
  pyenv local 3.6.15
  python -m venv Wav2LipEnv
  source Wav2LipEnv/bin/activate
  python3 --version
  ```

- **For Windows (using Anaconda):**
  ```
  conda create --name Wav2LipEnv python=3.6
  conda activate Wav2LipEnv
  ```

3. **Install Dependencies:**
```
pip install --upgrade pip
pip install opencv-contrib-python==4.2.0.34
pip install -r requirements.txt
```

4. **Download Pretrained Models:**
Download `wav2lip_gan.pth` from the repository and place it into the `checkpoints` folder.

## Usage

To lip-sync a video to any audio, run:
```
python inference.py --checkpoint_path path-to-wav2lip_gan.pth --face path-to-video.mp4 --audio path-to-audio.wav
```
The output will be saved in the `results` folder.

## Tips for Better Results

- Ensure the Python 3.6 environment is active.
- Use .mp4 format for video and .wav for audio.
- Lower quality videos (e.g., 1080p) tend to give better results.
- Ensure the video is not longer than the audio.
- For detailed settings, refer to the official [Wav2Lip repository](https://github.com/Rudrabha/Wav2Lip.git).
