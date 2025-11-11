# AI Meeting Summarizer

AI meeting summarization notebook: transcribes audio via Whisper, cleans text, summarizes with BART/T5. Includes audio tools, ROUGE metrics, upload interface, multi-language support, GPU acceleration, key point extraction.

## Features

- **Speech Recognition**: Uses OpenAI Whisper for multi-language audio transcription
- **Text Summarization**: Implements BART and T5 transformer models for high-quality summaries
- **Audio Processing**: Supports various audio formats with chunking for long recordings
- **Text Preprocessing**: Cleans transcripts by removing filler words and noise
- **Evaluation**: ROUGE metrics for summary quality assessment
- **Interactive Interface**: Jupyter-based file upload and processing interface
- **GPU Acceleration**: Optimized for CUDA-enabled GPUs

## How It Works

This project is implemented as a comprehensive Jupyter notebook (`meetingsummarizer.ipynb`) that follows a structured pipeline for meeting summarization:

1. **Environment Setup**: Automatically installs and configures all required dependencies, resolving compatibility issues for GPU acceleration and CUDA libraries.

2. **Model Initialization**: Loads OpenAI Whisper for speech recognition and BART/T5 models for text summarization, with automatic device detection (CPU/GPU).

3. **Audio Processing**: Handles various audio formats, performs feature extraction, and chunks long recordings for efficient processing.

4. **Speech-to-Text Conversion**: Transcribes audio files into text using Whisper, supporting multiple languages and automatic language detection.

5. **Text Preprocessing**: Cleans raw transcripts by removing filler words, timestamps, and normalizing text for better summarization quality.

6. **Summarization**: Generates concise summaries using transformer models, with configurable length and quality parameters.

7. **Evaluation and Testing**: Includes built-in testing with sample data and ROUGE metrics for quality assessment.

8. **Interactive Interface**: Provides a user-friendly file upload interface for processing audio files directly within the notebook.

The notebook is designed to run end-to-end, from audio input to final summary output, with comprehensive error handling and progress reporting.

## Installation

This notebook is specifically designed to run on the Kaggle platform due to its optimized environment for machine learning workloads:

1. **Create a Kaggle Account**: Sign up at https://www.kaggle.com if you don't have an account.

2. **Create a New Notebook**:
   - Go to https://www.kaggle.com/code
   - Click "New Notebook"
   - Select "Python" as the environment

3. **Upload the Notebook**:
   - Download `meetingsummarizer.ipynb` from this repository
   - In Kaggle, click "File" > "Upload Notebook" or paste the code directly

4. **Enable GPU Acceleration**:
   - In the notebook settings (right panel), enable "GPU" accelerator
   - Select "T4 x2" or "P100" GPU option (see Platform Requirements below)

5. **Internet Access**:
   - Ensure internet is enabled in notebook settings for downloading models and datasets

The notebook includes automated dependency installation and environment setup, so no manual pip installs are required.

## Platform Requirements

This system is optimized for and tested exclusively on the Kaggle platform, which provides the necessary computational resources and pre-configured environment for machine learning workloads.

### Required Environment:
- **Platform**: Kaggle Notebooks (https://www.kaggle.com)
- **GPU Accelerator**: 
  - T4 x2 (recommended - tested and verified to work without issues)
  - P100 (alternative option with sufficient VRAM)
- **Internet Access**: Enabled for model/dataset downloads
- **Session Time**: Adequate time allocation (recommended: 9+ hours for full processing)

### Technical Requirements:
- Python 3.8+
- PyTorch 2.1.0+ with CUDA 11.8 support
- Transformers 4.35.0+
- OpenAI Whisper (base model or larger)
- Audio processing libraries (Librosa, SoundFile, SciPy)
- NLP libraries (NLTK, ROUGE-Score)
- Jupyter Notebook with ipywidgets support

### Hardware Specifications:
- **GPU Memory**: Minimum 16GB VRAM (T4 x2 provides ~32GB effective)
- **RAM**: 16GB+ system RAM
- **Storage**: Sufficient for model downloads (~5-10GB)

**Note**: The system may not function properly on local machines or other cloud platforms due to dependency conflicts and CUDA version incompatibilities. Kaggle's managed environment ensures consistent performance and compatibility.

## Usage

1. **Audio Processing**: Upload audio files (.wav, .mp3, .mp4, etc.) through the interface
2. **Transcription**: Automatic speech-to-text conversion
3. **Summarization**: Generate concise meeting summaries
4. **Key Points**: Extract important points and action items

### Example Code:
```python
from meetingsummarizer import MeetingSummarizationPipeline

pipeline = MeetingSummarizationPipeline()
results = pipeline.process_audio_file('path/to/meeting.wav')
print(results['summary'])
```

## Configuration

- **Whisper Model**: Choose from tiny, base, small, medium, large
- **Summarizer Model**: facebook/bart-large-cnn (default) or T5 variants
- **Summary Length**: Adjustable min/max lengths
- **Language**: Auto-detect or specify language

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Disclaimer

See [DISCLAIMER.md](DISCLAIMER.md) for important usage notices and limitations.

## Contact

For questions or contributions:
- **Phone**: +91 9491149955
- **Email**: gbindra21@gmail.com

## Contributing

Contributions are welcome! Please read the disclaimer and ensure your code follows the project's standards.
