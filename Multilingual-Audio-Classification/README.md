# Multilingual Audio Classification with Language Identification

This project was developed as part of the "Natural Language Processing / Audio Processing" course of my Master's in Applied Data Science and AI.

It evaluates the performance of a language identification model across multiple languages using audio classification with transformer-based models, with a focus on assessing performance for Italian (my mother tongue).

## Technologies Used
- Python (Jupyter Notebook)
- Hugging Face Transformers
- Librosa (Audio processing)
- Whisper FLEURS Language ID model
- Google Colab

## Project Overview

The assignment required assessing a language identification model's performance on Italian vs. non-Italian speech. I expanded this by testing the model across **multiple languages** to evaluate its robustness and accuracy in multilingual scenarios.

The project implements:
- Audio preprocessing and feature extraction
- Language classification across 5 languages
- Performance evaluation using classification accuracy
- Comparative analysis of model confidence across different languages

## Dataset

**Languages tested:**
- **Italian** (mother tongue) - 10 samples
- **English** - 3 samples
- **Spanish** - 3 samples  
- **French** - 2 samples
- **Dutch** - 2 samples

**Total:** 20 audio samples across 5 languages

All audio files were either personally recorded or sourced from the internet to ensure diverse accents and speaking styles.

## How to Use

1. Upload or reference the audio files (organized by language).
2. Open the notebook in Google Colab.
3. Run all cells sequentially.
4. The model will:
   - Process each audio file
   - Predict the language with confidence scores
   - Display results for each language category

## How to Reproduce the Results

- Ensure all audio files are accessible (uploaded to Colab or linked).
- Run all cells as is.
- The notebook outputs:
  - Language predictions for each audio sample
  - Confidence scores for top predictions
  - Language-by-language results grouped for comparison

## Technical Highlights

- **Model:** Whisper FLEURS Language ID (sanchit-gandhi/whisper-medium-fleurs-lang-id)
- **Architecture:** Whisper-based audio classification model trained on 100+ languages
- **Task:** Multi-class language identification from speech audio
- **Evaluation:** Prediction accuracy and confidence score analysis across languages

## Key Findings

- The model demonstrated strong performance across all tested European languages.
- Italian samples (mother tongue) provided a quality control baseline with native speaker verification.
- Cross-language testing revealed the model's robustness in multilingual scenarios.
- Confidence scores varied by language, with some languages showing more consistent predictions than others.

## Notes

- This project went beyond assignment requirements by testing multiple non-Italian languages for comprehensive evaluation.
- Audio quality, background noise, and accent variations can impact classification accuracy.
- The multilingual approach demonstrates practical audio processing capabilities for real-world language detection systems.

## Author

Silvia Garavaglia  
[LinkedIn](https://www.linkedin.com/in/silviagaravaglia/) | [GitHub](https://github.com/silviagara)

---

**📦 Final Project Structure:**

```
Multilingual-Audio-Classification/
├── Multilingual-Audio-Classification.ipynb
├── README.md
└── audio_samples/ (optional)
    ├── italian/
    ├── english/
    ├── spanish/
    ├── french/
    └── dutch/
```
