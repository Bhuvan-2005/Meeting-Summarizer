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

## Installation

1. Clone this repository:
```bash
git clone https://github.com/Bhuvan-2005/meeting-summarizer.git
cd meeting-summarizer
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Open the Jupyter notebook:
```bash
jupyter notebook meetingsummarizer.ipynb
```

## Requirements

- Python 3.8+
- PyTorch 2.1.0+ (with CUDA support for GPU acceleration)
- Transformers 4.35.0+
- OpenAI Whisper
- Librosa, SoundFile, SciPy
- NLTK, Datasets, ROUGE-Score
- Jupyter Notebook
- ipywidgets

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
