# SETUP.md

### 1\. System Prerequisites

Before running any Python code, you must install **FFmpeg**. The audio processing libraries rely on this software to read and write media files.

  * **Mac:** `brew install ffmpeg`
  * **Windows:** `winget install ffmpeg` (or download from [ffmpeg.org](https://ffmpeg.org/))
  * **Linux:** `sudo apt install ffmpeg`

-----

### 2\. Initialize Repository

Run the following commands in your terminal to create the necessary directory structure and empty documentation files.

```bash
mkdir restoring-robinson
cd restoring-robinson
mkdir -p data/raw data/processed data/output docs notebooks

# Create documentation files
touch README.md
touch docs/found_audio_sources.md
touch docs/commercial_workflow.md

# Create the requirements file
touch requirements.txt
```

-----

### 3\. Create Requirements File

Copy the following content into the `requirements.txt` file you just created.

```text
# --- Core AI Libraries ---
openai-whisper          # Transcription
demucs                  # Audio separation (removing noise)
coqui-tts               # Voice Cloning (The maintained fork of Coqui)

# --- Audio Processing Utilities ---
pydub                   # Easy audio manipulation (slicing/saving)
ffmpeg-python           # Python bindings for FFmpeg
soundfile               # Reading/writing audio files
librosa                 # Audio analysis

# --- Notebook Support ---
ipykernel               # Required to run the notebook
jupyter                 # Jupyter interface
```

-----

### 4\. Installation & Environment Setup

**CRITICAL NOTE:** Do not simply run `pip install` if you have an NVIDIA GPU. You must install PyTorch first to enable hardware acceleration.

#### Option A: NVIDIA GPU Users (Recommended)

This ensures the AI models run on your graphics card (much faster).

```bash
# 1. Install PyTorch with CUDA support explicitly
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118

# 2. Then install the project requirements
pip install -r requirements.txt
```

#### Option B: Mac (M1/M2/M3) or CPU Users

Mac users will automatically use "MPS" (Metal Performance Shaders) for acceleration.

```bash
pip install -r requirements.txt
```

-----

### 5\. Running the Project

Once installed, place your raw MP3s into the `data/raw/` folder and launch the notebook:

```bash
jupyter notebook notebooks/01_restoration_pipeline.ipynb
```