
# Emotion-Aware Speech Recognition

This Python project performs **emotion-aware speech recognition** using a combination of [OpenAI Whisper](https://github.com/openai/whisper) for transcription and **SVM-based emotion detection** using audio features (MFCC + pitch).

---

## 🚀 Features

- 🎙️ Transcribes speech from `.mp4` files using Whisper
- 📊 Extracts MFCC and pitch-based audio features
- 😃 Classifies speaker emotion (happy, sad, angry, neutral)
- 🎞️ Converts video/audio files (MP4) to WAV format for processing

---

## 📦 Requirements

Make sure you have Python 3.7+ installed. Install the required libraries:

```bash
pip install openai-whisper librosa scikit-learn moviepy numpy
```

Install `ffmpeg` (required by Whisper and moviepy):

- **Ubuntu/Debian**:
  ```bash
  sudo apt install ffmpeg
  ```
- **macOS (Homebrew)**:
  ```bash
  brew install ffmpeg
  ```
- **Windows**:
  Download from: https://ffmpeg.org/download.html and add it to PATH.

---

## 🧠 How It Works

1. **convert_mp4_to_wav**: Extracts audio from an MP4 file using MoviePy.
2. **transcribe_audio**: Transcribes the audio using Whisper (`base` model).
3. **extract_audio_features**: Uses `librosa` to compute MFCC and pitch features.
4. **train_emotion_classifier**: Simulates training of an SVM emotion classifier.
5. **classify_emotion**: Predicts the emotional tone of the speaker.

---

## 📁 File Structure

```
emotion_aware_speech_recognition/
├── main.py         # All processing code
└── README.md       # Project documentation
```

---

## 🧪 Example Usage

Ensure `main.py` contains the following at the bottom:

```python
audio_path = "/content/sample.mp4"
emotion_aware_speech_recognition(audio_path)
```

Run the script:

```bash
python main.py
```

Expected output:

```
Transcription: Hello, how are you?
Detected Emotion: happy
Language Detected: en
```

---

## ⚠️ Notes

- The SVM classifier uses randomly generated features for demo purposes.
- For real use, train with labeled emotion data (e.g., RAVDESS, CREMA-D datasets).
- Whisper supports multilingual audio and automatically detects language.

---

## 📬 Author

Created with ❤️ using Python, OpenAI Whisper, and Librosa.

---

## 📄 License

This project is licensed under the MIT License – feel free to use, modify, and distribute it.
