<h1>
  <img src="./docs/images/icon.png" width="50" align="left" style="margin-right: 10px;">
 SmartVoice-AI-Suite
</h1>

<br clear="left"/>

[![Rust](https://img.shields.io/badge/rust-1.70+-orange.svg)](https://www.rust-lang.org)
[![License](https://img.shields.io/badge/license-Apache2-blue.svg)](LICENSE)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)]()

A high-performance, enterprise-grade speech recognition system built in Rust, powered by the VOSK speech recognition toolkit. Convert audio files to text with exceptional accuracy and speed.

### <img src="./docs/images/icon.png" width="24" align="top"> Key Features

- `High Accuracy`: Leverages VOSK's state-of-the-art speech recognition models
- `Fast Processing`: Optimized Rust implementation with efficient memory management
- `Real-time Progres`: Live progress tracking during audio processing
- `Multiple Formats`: Support for various audio file formats
- `Cross-Platform`: Works on Windows and Linux systems
- `Batch Processing`: Command-line interface for automated workflows
- `Interactive Mode`: User-friendly interactive interface
- `Robust Error Handling`: Comprehensive error management and validation

### <img src="./docs/images/icon.png" width="24" align="top"> Technical Stack

- `Language`: Rust (Edition 2024)
- `Speech Engine`: VOSK 0.3.1
- `Audio Processing`: Custom high-performance audio processor
- `Architecture`: Modular design with separated concerns

### <img src="./docs/images/icon.png" width="24" align="top"> Prerequisites

- Rust 1.70 or higher
- VOSK model files (download from [VOSK Models](https://alphacephei.com/vosk/models))

### ️<img src="./docs/images/icon.png" width="24" align="top"> Supported Audio Formats

| Format | Sample Rate | Bit Depth | Channels |
|--------|-------------|-----------|----------|
| WAV    | 8-48 kHz    | 16-bit    | Mono/Stereo |
| MP3    | 8-48 kHz    | Variable  | Mono/Stereo |
| FLAC   | 8-192 kHz   | 16-24 bit | Mono/Stereo |
| OGG    | 8-48 kHz    | Variable  | Mono/Stereo |

### <img src="./docs/images/icon.png" width="24" align="top"> Installation

#### 1️⃣ Clone the Repository
```bash
git clone https://github.com/dsddevs/SmartVoice-AI-Suite.git
cd SmartVoice-AI-Suite
```

#### 2️⃣ Download VOSK Model
Download a VOSK model suitable for your language:
```bash
# Example for English model
wget https://alphacephei.com/vosk/models/vosk-model-en-us-0.22.zip
unzip vosk-model-en-us-0.22.zip
```

#### 3️⃣ Build the Project
```bash
cargo build --release
```

### <img src="./docs/images/icon.png" width="24" align="top"> Usage

```bash
# Variant 1
cargo run -- <vosk-model path> <audio file path>
```

```bash

# Variant 2
cargo run
Enter the path to the VOSK model: <vosk-model path> 
Enter the path to the audio file: <audio file path>
```
### <img src="./docs/images/icon.png" width="24" align="top"> Project Structure

```
SmartVoice-AI-Suite/
├── src/
│   ├── main.rs              # Entry point and CLI handling
│   ├── audio_processor.rs   # Audio processing and chunking
│   ├── speech_recognizer.rs # VOSK integration and recognition
│   └── file_handler.rs      # Output file management
├── models/                  # VOSK model storage
├── audio/                   # Sample audio files
├── output/                  # Generated transcriptions
├── Cargo.toml               # Dependencies and metadata
├── build.rs                 # Build configuration
└── README.md                # This file
```

### <img src="./docs/images/icon.png" width="24" align="top"> Configuration

The system uses the following default settings:
- ```Sample Rate```: 16,000 Hz
- ```Chunk Size```: 16,384 bytes
- ```Max Alternatives```: 1
- ```Word-level timestamps```: Disabled for optimal performance

### <img src="./docs/images/icon.png" width="24" align="top"> Performance

- `Processing Speed`: Real-time or faster depending on hardware
- `Memory Usage`: Optimized for large audio files
- `Supported File Sizes`: No practical limit (streaming processing)
- `Progress Tracking`: Real-time progress updates every 10 chunks

### <img src="./docs/images/icon.png" width="24" align="top"> Supported Languages

Supports any language with available VOSK models:
- English (US/UK)
- Russian
- German
- French
- Spanish
- Chinese
- And many more...

### <img src="./docs/images/icon.png" width="24" align="top"> Output

```
=== Speech recognition system ===
The model is used: /models/vosk-model-en-us-0.22
Processing audio file: /audio/meeting.wav
Audio file size: 15728640 bytes
PROGRESS: 10.0%
PROGRESS: 20.0%
...
PROGRESS: 100.0%
Successfully created text file: /audio/text_meeting.txt
Recognition completed successfully!
```

### <img src="./docs/images/icon.png" width="24" align="top"> License
This project is licensed under the Apache-2 License - see the [LICENSE](LICENSE) file for details.

### <img src="./docs/images/icon.png" width="24" align="top"> Contact
- 📧 dsddevs@gmail.com
- <img src="./docs/images/telegram.png" width="24" valign="middle"> @dsddevs / +998906006989


### <img src="./docs/images/icon.png" width="24" align="top"> Acknowledgments

- [VOSK](https://alphacephei.com/vosk/) for the excellent speech recognition toolkit
- Rust community for the amazing ecosystem
- Contributors and testers

