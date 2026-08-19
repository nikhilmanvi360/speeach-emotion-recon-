# 🎙️ Speech Emotion Recognition

A browser-based **Speech Emotion Recognition (SER)** platform that analyzes human speech and estimates the emotional state expressed through vocal characteristics.

The system combines **digital signal processing (DSP), acoustic feature extraction, MFCC analysis, emotion classification concepts, dataset benchmarking, model architecture exploration, and interactive visualization** into a single interface.

## 🚀 Features

* 🎙️ Record speech directly from the browser
* 📂 Upload audio samples
* 🔊 Built-in emotional speech samples
* 😊 Emotion classification across 8 emotion categories
* 📊 Emotion probability distribution
* 🎚️ Valence-Arousal-Dominance (VAD) visualization
* 🎵 Mel-spectrogram visualization
* 📈 Waveform / energy visualization
* 🎼 MFCC visualization
* 🔬 Acoustic feature inspection
* 🎯 Fundamental frequency / pitch analysis
* ⚡ RMS energy analysis
* 📐 Zero-crossing rate analysis
* 🔊 Spectral centroid and rolloff
* 📊 Spectral flatness
* 🎛️ Jitter and shimmer estimation
* 🧠 Model architecture explorer
* 🧪 Dataset benchmark comparison
* 📄 Export analysis as JSON
* 📑 Export acoustic features as CSV
* 🌐 Browser-based audio processing

## 🎭 Supported Emotions

The system supports:

```text
Happy
Angry
Sad
Neutral
Fearful
Disgusted
Surprised
Calm
```

## 🧠 System Architecture

The overall analysis pipeline can be represented as:

```text
Audio Input
    │
    ├── Microphone Recording
    ├── Uploaded Audio
    └── Built-in Sample
    │
    ▼
Audio Buffer
    │
    ▼
Digital Signal Processing
    │
    ├── Pitch / F0
    ├── RMS Energy
    ├── Zero Crossing Rate
    ├── Spectral Centroid
    ├── Spectral Rolloff
    ├── Spectral Flatness
    ├── MFCC
    ├── Mel Spectrogram
    ├── Chroma
    ├── Jitter
    └── Shimmer
    │
    ▼
Acoustic Analysis
    │
    ├── Emotion Characteristics
    ├── Prosody
    └── Vocal Characteristics
    │
    ▼
Emotion Analysis
    │
    ├── Primary Emotion
    ├── Confidence
    ├── Probability Distribution
    └── VAD Coordinates
    │
    ▼
Interactive Results Dashboard
```

## 🔬 Digital Signal Processing

One of the major components of this project is its browser-based DSP engine.

The system extracts several acoustic characteristics from the speech signal.

### Fundamental Frequency

The fundamental frequency (`F0`) provides information about vocal pitch.

```text
Pitch → F0 → Pitch contour → Pitch variation
```

Pitch characteristics can help distinguish emotional speech patterns.

### RMS Energy

RMS energy provides an estimate of vocal intensity.

Higher vocal energy can be associated with emotionally intense speech, while lower energy can indicate subdued speech.

### Zero Crossing Rate

Zero Crossing Rate measures how frequently the audio waveform crosses zero amplitude.

It can provide information about signal characteristics and spectral content.

### Spectral Centroid

The spectral centroid estimates where the center of spectral energy is located.

It can help characterize the perceived brightness of speech.

### Spectral Rolloff

Spectral rolloff estimates the frequency below which a chosen proportion of spectral energy is concentrated.

### Spectral Flatness

Spectral flatness provides an indication of how noise-like or tonal a signal is.

## 🎼 MFCC Analysis

The project extracts **Mel-Frequency Cepstral Coefficients (MFCCs)** from speech.

MFCCs are widely used in speech-processing systems because they provide a compact representation of the spectral characteristics of human speech.

The application provides:

* MFCC matrix
* Mean MFCC coefficients
* MFCC visualization
* Acoustic feature export

Conceptually:

```text
Audio
 ↓
Frame Blocking
 ↓
Spectrum
 ↓
Mel Filter Bank
 ↓
Log Energy
 ↓
DCT
 ↓
MFCC
```

## 🌈 Mel-Spectrogram

The application generates a mel-spectrogram representation of the audio signal.

Users can inspect how spectral energy changes over time and frequency.

```text
Frequency
   ↑
   │ ███
   │ ██████
   │  ███████
   │    █████
   │
   └────────────────→ Time
```

## 🎚️ Acoustic Feature Dashboard

The system exposes extracted acoustic characteristics instead of hiding the analysis behind a single emotion label.

Available features include:

| Feature           | Description                    |
| ----------------- | ------------------------------ |
| Duration          | Length of audio                |
| Sample Rate       | Audio sampling frequency       |
| RMS Energy        | Signal energy                  |
| Maximum Energy    | Peak energy                    |
| Pitch / F0        | Fundamental frequency          |
| Pitch Variance    | Pitch variability              |
| ZCR               | Zero-crossing rate             |
| Spectral Centroid | Spectral center                |
| Spectral Rolloff  | Spectral energy boundary       |
| Spectral Flatness | Tonality/noise characteristic  |
| MFCC              | Speech spectral representation |
| Mel Spectrogram   | Time-frequency representation  |
| Chroma            | Pitch-class representation     |
| HNR               | Harmonics-to-noise estimate    |
| Jitter            | Pitch perturbation             |
| Shimmer           | Amplitude perturbation         |

## 🧠 Emotion Representation

Instead of returning only:

```text
Emotion = Angry
```

the application maintains a richer representation.

Example:

```text
Primary Emotion
      +
Confidence
      +
Emotion Probabilities
      +
VAD Coordinates
      +
Prosody
      +
Acoustic Features
```

### Valence-Arousal-Dominance

The system represents emotional state using three dimensions:

```text
Valence
Negative ←────────→ Positive

Arousal
Calm     ←────────→ Excited

Dominance
Submissive ←──────→ Dominant
```

This allows emotions to be represented as a continuous emotional space rather than only discrete labels.

## 🧪 Dataset Benchmarking

The application provides information and comparison capabilities for multiple speech-emotion datasets:

* **RAVDESS**
* **TESS**
* **EMO-DB**

Dataset information includes:

* Dataset name
* Institution
* Language
* Speaker information
* Number of samples
* Emotion categories
* Sample rate
* Model accuracy context
* Typical acoustic characteristics

## 🤖 Model Architecture Explorer

The project provides an interactive exploration of several commonly used architectures for speech emotion recognition:

```text
CNN 2D
Bi-LSTM
CRNN
CNN 1D + GRU
```

The architecture explorer exposes model characteristics such as:

* Architecture type
* Layer pipeline
* Parameter count
* Estimated inference latency
* Dataset accuracy context
* Feature focus

This makes the project useful not only as an application but also as an educational tool for understanding SER model architectures.

## 🎙️ Audio Input

The system supports multiple input methods.

### Browser Microphone

Users can record speech directly through the browser microphone.

```text
Microphone
    ↓
MediaRecorder
    ↓
Audio Buffer
    ↓
DSP Analysis
```

### Audio Upload

Existing audio recordings can also be loaded into the application.

### Built-in Samples

The project includes predefined emotional speech samples for experimentation and demonstration.

## 📊 Results Dashboard

After processing an audio sample, the dashboard provides:

* Detected emotion
* Confidence
* Emotion probabilities
* VAD position
* Prosody summary
* Acoustic insights
* Model comparison
* Dataset benchmark context
* DSP features

Results can also be exported.

### JSON Export

Complete analysis results can be exported as JSON.

### CSV Export

Extracted acoustic and MFCC statistics can be exported as CSV.

## 🛠️ Tech Stack

| Technology        | Purpose                         |
| ----------------- | ------------------------------- |
| React             | User interface                  |
| TypeScript        | Application logic               |
| Vite              | Development & build tooling     |
| Web Audio API     | Audio capture and processing    |
| HTML5 Canvas      | Audio visualization             |
| Tailwind CSS      | UI styling                      |
| Lucide React      | Interface icons                 |
| Express           | Local server                    |
| Google Gemini API | Multimodal analysis integration |

## 📁 Project Structure

```text
speech-emotion-recognition/
│
├── src/
│   ├── components/
│   │   ├── AudioCapture.tsx
│   │   ├── EmotionResultsDashboard.tsx
│   │   ├── SpectrogramMFCCViewer.tsx
│   │   ├── AcousticFeaturesTable.tsx
│   │   ├── DatasetBenchmarkView.tsx
│   │   └── ModelArchitectureExplorer.tsx
│   │
│   ├── data/
│   │   └── datasets.ts
│   │
│   ├── utils/
│   │   └── dspEngine.ts
│   │
│   ├── App.tsx
│   ├── main.tsx
│   ├── index.css
│   └── types.ts
│
├── assets/
├── index.html
├── server.ts
├── vite.config.ts
├── package.json
├── tsconfig.json
└── README.md
```

## ⚙️ Installation

### Prerequisites

* Node.js
* npm
* Modern browser with microphone support for live recording

### Clone

```bash
git clone https://github.com/<your-username>/speech-emotion-recognition.git
cd speech-emotion-recognition
```

### Install Dependencies

```bash
npm install
```

### Environment Variables

Create a `.env.local` file and configure the required Gemini API key if using the multimodal analysis functionality:

```env
GEMINI_API_KEY=your_api_key_here
```

> Never commit your API key to GitHub.

### Start Development Server

```bash
npm run dev
```

Open the local URL provided by the development server.

## 🏗️ Production Build

```bash
npm run build
```

Preview the production build:

```bash
npm run preview
```

## 🧪 Example Workflow

```text
1. Select a dataset
       ↓
2. Record / upload / select sample
       ↓
3. Decode audio
       ↓
4. Extract DSP features
       ↓
5. Calculate MFCCs
       ↓
6. Generate spectrogram
       ↓
7. Analyze acoustic characteristics
       ↓
8. Estimate emotional state
       ↓
9. Compare model architectures
       ↓
10. Display results
       ↓
11. Export analysis
```

## 🎯 Learning Objectives

This project demonstrates practical concepts in:

* Speech processing
* Digital signal processing
* Machine learning concepts
* Speech emotion recognition
* MFCC extraction
* Spectrogram analysis
* Audio feature engineering
* Prosody analysis
* Emotion representation
* Model architecture comparison
* Dataset benchmarking
* Browser-based audio processing
* React + TypeScript application development

## ⚠️ Important Note

Speech emotion recognition is inherently difficult.

Emotional expression varies significantly between speakers, languages, cultures, recording environments, and speaking styles.

Therefore, an emotion prediction should be treated as an **estimate**, not a definitive measurement of a person's internal emotional state.

Dataset benchmark numbers shown by the application are contextual information and should not be interpreted as guaranteed real-world performance.

## 🚧 Limitations

* Acoustic features alone cannot perfectly determine human emotion.
* Dataset characteristics can strongly influence model performance.
* Real-world speech is significantly more diverse than controlled datasets.
* Microphone quality and background noise can affect extracted features.
* Emotion labels are subjective and dataset-dependent.

## 🔮 Future Improvements

* [ ] Train a dedicated CNN/CRNN model on RAVDESS
* [ ] Add real trained model inference
* [ ] Add noise reduction
* [ ] Add voice activity detection
* [ ] Add speaker normalization
* [ ] Add real-time streaming emotion analysis
* [ ] Add multilingual emotion recognition
* [ ] Add confusion matrices
* [ ] Add ROC/AUC evaluation
* [ ] Add model accuracy benchmarking
* [ ] Add explainable emotion predictions
* [ ] Add attention visualization for deep learning models
* [ ] Add batch audio analysis
* [ ] Add REST API for external applications

## 📜 License

This project is intended for educational, research, and portfolio purposes.

---

⭐ If you found this project useful, consider starring the repository.
