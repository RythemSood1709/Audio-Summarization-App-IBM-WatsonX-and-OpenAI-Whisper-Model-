# Audio Summarization App
Powered by OpenAI Whisper & IBM watsonx.ai
📖 Overview
This repository contains a high-performance Audio Analysis Pipeline. It bridges the gap between raw audio data and actionable insights by utilizing OpenAI's Whisper for state-of-the-art transcription and IBM watsonx.ai for context-aware summarization.

🛠️ Tech Stack
Transcription: OpenAI Whisper (Large-v3/Medium via transformers)

LLM Orchestration: IBM watsonx.ai

Compute: PyTorch (with CUDA support for fast GPU inference)

Frontend: Gradio for a clean, browser-based interface

🚀 Getting Started
1. Prerequisites
Ensure you have FFmpeg installed on your system for audio processing:

Bash
# Ubuntu
sudo apt install ffmpeg

# MacOS
brew install ffmpeg

#2. Installation

Bash
# Clone the repository
git clone https://github.com/RythemSood1709/Audio-Summarization-App-IBM-WatsonX-and-OpenAI-Whisper-Model-.git
cd Audio-Summarization-App-IBM-WatsonX-and-OpenAI-Whisper-Model-

# Install dependencies
pip install -r requirements.txt

# 3. Setup Credentials
Create a .env file in the root directory:

# Code snippet
WATSONX_APIKEY=your_ibm_api_key

PROJECT_ID=your_project_id

URL=https://us-south.ml.cloud.ibm.com

# 4. Running the App
The main entry point for the application is speech_analyser.py.

Bash
python speech_analyser.py
⚙️ Workflow
Audio Input: Upload .mp3, .wav, or .m4a through the Gradio interface.

Transcription: Torch loads the Whisper model to convert audio to text locally.

Summarization: The transcript is passed to an IBM watsonx model (like granite-13b-instruct or llama-3) to generate a concise summary.

Result: View both the full transcript and the AI-generated summary side-by-side.

📁 Project Structure
Plaintext
.
├── speech_analyser.py   # Main application script
├── requirements.txt      # Project dependencies
├── .env                  # Environment variables (API Keys)
└── README.md             # Project documentation
🤝 Contributing
Fork the Project

Create your Feature Branch (git checkout -b feature/NewFeature)

Commit your Changes (git commit -m 'Add NewFeature')

Push to the Branch (git push origin feature/NewFeature)

Open a Pull Request
