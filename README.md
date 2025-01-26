# Text-to-Speech (TTS) Application

This project is a Text-to-Speech (TTS) application that converts text into speech using advanced TTS models. It consists of a FastAPI backend and a React frontend, providing a user-friendly interface for generating and playing audio files.

## Features

- **Text-to-Speech Conversion**: Convert any text into speech using the `TTS` library.
- **Customizable Parameters**: Adjust various parameters like speed, sampling rate, temperature, noise scale, and more to fine-tune the audio output.
- **Audio Playback**: Play the generated audio directly in the browser.
- **Static File Serving**: The backend serves generated audio files from a static directory.





## Usage

1. Open the application in your browser at `http://localhost:3000`.
2. Enter the text you want to convert into speech.
3. Adjust the parameters (speed, sampling rate, temperature, etc.) as needed.
4. Click "Convert to Speech" to generate the audio.
5. The generated audio will be played automatically, and you can download it if needed.

## API Endpoints

### Convert Text to Speech

- **URL**: `/api/v1/tts/convert`
- **Method**: `POST`
- **Request Body**:
  ```json
  {
    "text": "Your text here",
    "speed": 1.0,
    "sampling_rate": 44100,
    "temperature": 0.7,
    "noise_scale": 0.667,
    "noise_scale_w": 0.8
  }
  ```
- **Response**:
  ```json
  {
    "file_path": "/static/some-uuid.mp3"
  }
  ```

