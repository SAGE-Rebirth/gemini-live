# Gemini Live Cam – Project Guide

## Overview

Gemini Live Cam is a Python application that streams real-time audio (and optionally video or screen captures) from your device to Google Gemini using the Gemini Live API. It enables interactive conversations with Gemini via both text and voice, demonstrating how to integrate media capture, streaming, and AI-powered responses in Python.

---

## Features

- Real-time audio streaming to Gemini with AI-powered voice responses.
- Optional video or screen frame streaming.
- Interactive text chat with Gemini.
- Audio playback of Gemini's responses.
- Extensible for UI integration (Flask, Streamlit, etc.).

---

## Setup Instructions

### 1. Clone the Repository

```sh
git clone <your-repo-url>
cd gemini-live-cam
```

### 2. Create and Activate a Virtual Environment

**Windows:**
```sh
python -m venv gem-env
gem-env\Scripts\activate
```
**Linux/macOS:**
```sh
python3 -m venv gem-env
source gem-env/bin/activate
```

### 3. Install Dependencies

```sh
pip install google-genai opencv-python pyaudio pillow mss python-dotenv
```

### 4. Set Up Environment Variables

- Create a `.env` file in the project root.
- Add your Google Gemini API key:

```
GEMINI_API_KEY=your_google_gemini_api_key_here
```

---

## Running the Project

### Audio + Camera Mode

```sh
python gemini-live-cam.py --mode camera
```

### Audio + Screen Mode

```sh
python gemini-live-cam.py --mode screen
```

### Audio Only

```sh
python gemini-live-cam.py --mode none
```

---

## How It Works

- The script captures audio from your microphone and (optionally) video from your webcam or screen.
- Audio and video/screen frames are streamed to the Gemini model using the Google GenAI Live API.
- You can also interact with Gemini via text input in the console.
- Gemini responds with audio, which is played back in real time.

---

## Requirements

- Python 3.8+
- A working microphone (and webcam/screen for video/screen modes)
- Google Gemini API key

---

## Significance

This project demonstrates how to:
- Integrate real-time media capture (audio/video/screen) in Python.
- Stream data to a state-of-the-art AI model using Google GenAI Live API.
- Build the foundation for advanced AI-powered assistants, bots, or interactive applications.

---

## Next Steps

- Extend with a web UI (Flask/Streamlit).
- Add more controls and error handling.
- Integrate with other tools or APIs as needed.

---

## References

- [Google Gemini Cookbook – Live API Quickstart](https://github.com/google-gemini/cookbook/blob/main/quickstarts/Get_started_LiveAPI.py)
- [Google GenAI Python SDK Documentation](https://ai.google.dev/api/python/google/genai/aio/live/LiveSession)

