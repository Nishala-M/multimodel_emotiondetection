
# Emotion-Aware Speech Recognition (Jupyter Notebook)

This project uses a Jupyter Notebook (`multimodelemotiondetection.ipynb`) to perform **emotion-aware speech recognition** using OpenAI's Whisper model for transcription and an SVM classifier for basic emotion detection based on audio features.

---

## 🚀 Features

- 🎙️ Transcribes speech from `.mp4` files using Whisper
- 📊 Extracts MFCC and pitch-based audio features using `librosa`
- 😃 Detects basic emotions: happy, sad, angry, neutral
- 🎞️ Converts video/audio files (MP4) to WAV format for processing

---

## 📦 Requirements

Before running the notebook, make sure to install the following dependencies:

```bash
pip install openai-whisper librosa scikit-learn moviepy numpy
```

Also, ensure `ffmpeg` is installed:

- **Ubuntu/Debian**:
  ```bash
  sudo apt install ffmpeg
  ```
- **macOS** (Homebrew):
  ```bash
  brew install ffmpeg
  ```
- **Windows**:
  Download from: https://ffmpeg.org/download.html and add it to your system PATH.

---

## 🧠 How It Works

1. **Convert Audio**: Extracts audio from an `.mp4` file to `.wav` using MoviePy.
2. **Speech Recognition**: Transcribes audio using Whisper (`base` model).
3. **Feature Extraction**: Extracts MFCC + pitch features with `librosa`.
4. **Emotion Detection**: A simple SVM classifier predicts the speaker's emotion.

---

## 📄 File Structure

```
emotion_aware_speech_recognition/
├── multimodelemotiondetection.ipynb  # Main notebook
└── README.md                         # Project documentation
```

---

## 🧪 How to Use

1. Open the notebook:

```bash
jupyter notebook multimodelemotiondetection.ipynb
```

2. Set the path to your `.mp4` audio/video file:

```python
audio_path = "/content/sample.mp4"
emotion_aware_speech_recognition(audio_path)
```

3. Run all cells and observe the outputs:
   - Transcription
   - Detected Emotion
   - Detected Language

---

## ⚠️ Notes

- The emotion classifier is trained on **synthetic data** as a placeholder.
- For production, use real datasets like RAVDESS, CREMA-D, or Emo-DB.
- Whisper automatically detects the language of the audio.

---

## 📬 Author

Created with ❤️ using Python, Whisper, Librosa, and Scikit-learn.

---

## 📄 License

This project is licensed under the MIT License. You are free to use, modify, and distribute it.
