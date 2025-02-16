# Introduction

This Python script is designed to synthesize speech using state-of-the-art open and closed-source tools. It's implemented in a single file to simplify deployment and usage.

# Features

- **ClosedAI TTS**
- **Coqui TTS**

# Installation

```
git clone https://github.com/Inc44/TheTTS.git
cd TheTTS
conda create --name TheTTS python=3.10.14
conda activate TheTTS
pip install openai==1.13.3 TTS==0.22.0
DS_BUILD_TRANSFORMER_INFERENCE=1 pip install deepspeed==0.14.0
sudo apt install git-lfs
git lfs install
git clone https://huggingface.co/coqui/XTTS-v2
sudo rm -r XTTS-v2/.git
cp /home/pc/github/TheTTS/xtts.py /home/pc/miniconda3/envs/TheTTS/lib/python3.10/site-packages/TTS/tts/models
```

# Usage

## Parameters

- `--api_key`: Use this flag to use ClosedAI's API.
- `--text_file_path`: The path to the text file input (default: ./input).
- `--speech_file_dir`: The directory where speech files will be saved (default:./result).
- `--speaker_wav`: The default speaker WAV file (default: en_sample.wav).
- `--language`: The language code (default: en).
- `--codec`: The audio codec to use (default: mp3).

## Commands

Execute the script from the command line, providing optional parameters if needed:

```bash
conda activate TheTTS
cd TheTTS
python -OO thetts.py [options]
```

# License

MIT
