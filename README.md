# Wav2Lip: Accurately Lip-syncing Videos In The Wild

Welcome to the Wav2Lip project! This repository contains the complete setup guide and instructions to use Wav2Lip, a model that can lip-sync videos to any target speech with high accuracy. The model works for any identity, voice, and language, and is based on the research paper: "A Lip Sync Expert Is All You Need for Speech to Lip Generation In The Wild", published at ACM Multimedia 2020.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.6
- Anaconda Navigator
- Git (Install using `conda install -c anaconda git`)

## Installation

Follow these steps to set up the Wav2Lip project:

1. **Create and Activate a New Environment:**
```
conda create --name Wav2LipEnv python=3.6
conda activate Wav2LipEnv
```

2. **Install Git:**
```
conda install -c anaconda git
```

3. **Clone Wav2Lip Repository:**
```
git clone https://github.com/Rudrabha/Wav2Lip.git
cd Wav2Lip
```

4. **Update pip and Install Required Libraries:**
```
python -m pip install --upgrade pip
pip install opencv-contrib-python==4.2.0.34
pip install -r requirements.txt
```

5. **Download Pretrained Model:**
- Download `wav2lip_gan.pth` (Wav2Lip + GAN Link) from the repository and place it into the `checkpoints` folder.

## Usage

To lip-sync a video to any audio, run:
```
python inference.py --checkpoint_path path-to-wav2lip_gan.pth --face path-to-video.mp4 --audio path-to-audio.wav
```
The final product should appear in the `results` folder.

## Tips for Using Wav2Lip on Windows:

- Ensure the `Wav2LipEnv` environment is activated and using Python 3.6 before running scripts.
- Video must be in .mp4 format and audio in .wav.
- Better results are obtained using lower quality video; 1080p looks best. 720p executes faster but may produce poorer results.
- Verify the Wav2Lip directory is correctly set up before proceeding.
- Make sure the video is not longer than the audio.
- Run the main script for synchronization in the Wav2Lip directory.
