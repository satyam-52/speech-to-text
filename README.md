# Hindi Audio Transcription and Translation

A Python script for Google Colab that transcribes Hindi audio files using OpenAI's Whisper model and translates the output to English using Google Translate API.

## Features

- 🎵 **Audio Transcription**: Uses Whisper Hindi Large-v2 model for accurate Hindi speech recognition
- 🔄 **Translation**: Translates Hindi text to English using Google Translate API
- 🚀 **GPU Support**: Automatically detects and uses GPU for faster processing
- 📁 **File Management**: Easy file upload, processing, and download in Google Colab
- 💾 **Multiple Outputs**: Saves both Hindi transcription and English translation
- 🎧 **Audio Playback**: Preview uploaded audio files before processing

## Requirements

- Google Colab environment
- Internet connection for model downloads and translation API

## Installation

Simply copy and paste the script into a Google Colab cell. The script will automatically install all required dependencies:

```python
!pip install transformers torch torchaudio accelerate googletrans==4.0.0rc1
```

## Dependencies

- `transformers` - For Whisper model
- `torch` & `torchaudio` - PyTorch for model inference
- `accelerate` - For optimized model loading
- `googletrans` - Google Translate API

## Usage

### Basic Usage

1. **Open Google Colab** and create a new notebook
2. **Copy and paste** the script into a cell
3. **Run the cell** to install dependencies and load models
4. **Upload your Hindi audio file** when prompted
5. **View results** - both Hindi transcription and English translation
6. **Download** the generated text files

### Supported Audio Formats

- WAV
- MP3
- M4A
- FLAC
- And other common audio formats supported by torchaudio

## Models Used

### Transcription Model
- **Model**: `vasista22/whisper-hindi-large-v2`
- **Type**: Fine-tuned Whisper model specifically for Hindi
- **Performance**: High accuracy for Hindi speech recognition

### Translation Model
- **Service**: Google Translate API
- **Language Pair**: Hindi (hi) → English (en)
- **Accuracy**: Excellent handling of proper nouns and context

## Example Output

**Input Audio**: Hindi speech saying "मेरा नाम सत्यम है"

**Hindi Transcription**: 
```
मेरा नाम सत्यम है
```

**English Translation**: 
```
My name is Satyam
```

## Script Structure

```python
# 1. Install dependencies
# 2. Initialize models (Whisper + Google Translate)
# 3. File upload interface
# 4. Audio transcription
# 5. Text translation
# 6. Results display and file download
```

## Key Functions

- `initialize_models()` - Loads both transcription and translation models
- `transcribe_and_translate_google()` - Main processing function
- `test_translation()` - Tests translation accuracy

## Performance Notes

- **GPU Recommended**: Script automatically uses GPU if available for faster processing
- **Processing Time**: Depends on audio length and hardware (typically 1-5 minutes for short clips)
- **Memory Usage**: Large model requires ~3GB GPU memory or ~6GB RAM

## Troubleshooting

### Common Issues

1. **Model Loading Errors**
   - Ensure stable internet connection
   - Restart runtime if memory issues occur

2. **Translation Errors**
   - Check if Google Translate service is accessible
   - Verify text encoding for special characters

3. **Audio Upload Issues**
   - Ensure audio file is in supported format
   - Check file size limits in Google Colab

### Error Messages

- `CUDA out of memory` → Restart runtime or use CPU
- `Translation failed` → Check internet connection
- `Audio format not supported` → Convert to WAV/MP3

## Alternative Translation Options

The script includes alternative translation models if Google Translate is not available:

- **Microsoft Translator**: Using `deep-translator` library
- **IndicTrans2**: Specialized for Indian languages
- **Helsinki-NLP**: Open-source option (less accurate for proper nouns)

## File Outputs

The script generates three files:
1. `*_hindi_transcription.txt` - Original Hindi text
2. `*_english_translation.txt` - Translated English text  
3. `*_transcription_and_translation.txt` - Combined results

## Contributing

Feel free to submit issues and enhancement requests!

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- OpenAI Whisper team for the base model
- Vasista22 for the Hindi fine-tuned model
- Google Translate for translation services
- Hugging Face for model hosting and transformers library

## Changelog

### v1.0.0
- Initial release with Whisper transcription
- Google Translate integration
- Google Colab optimization
- File management features

---

**Note**: This script is designed specifically for Google Colab. For local usage, modify the file upload/download sections accordingly.

---
Answer from Perplexity: pplx.ai/share
