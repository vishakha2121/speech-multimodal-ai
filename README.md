# 🎙️ Speech Multimodal AI

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104.0-green.svg)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-18.2.0-61DAFB.svg)](https://reactjs.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **A comprehensive, practice-ready, multilingual speech processing platform** that integrates state-of-the-art deep learning models (Whisper, wav2vec2, Conformer, Tacotron2) with Google's Gemini AI to deliver transcription, translation, speaker recognition, emotion detection, and voice synthesis.

---

## 🚀 Key Features

| Feature | Description | Technologies |
| :--- | :--- | :--- |
| **🎯 Speech-to-Text** | Accurately transcribe audio in multiple languages. | OpenAI Whisper, wav2vec2 |
| **🌍 Translation** | Translate transcribed speech between languages. | Google Gemini API, Custom Models |
| **👤 Speaker Recognition** | Identify and verify speakers from voice samples. | Conformer-based Embeddings |
| **😊 Emotion Detection** | Analyze emotional tone from vocal patterns. | Conformer, wav2vec2 |
| **🔊 Voice Synthesis** | Generate natural-sounding speech from text. | Tacotron2, WaveGlow Vocoder |

---

## 🏗️ Architecture Overview

This project follows a modular, service-oriented architecture designed for clarity and learning.



---

## 🛠️ Technology Stack

### Backend
- **Framework:** FastAPI (Python 3.10+)
- **Database:** SQLite (Development) / PostgreSQL (Production-ready)
- **ML/AI:** PyTorch, HuggingFace Transformers, OpenAI Whisper, Librosa, Tacotron2
- **APIs:** Google Gemini API, RESTful APIs, WebSockets
- **Caching:** Redis
- **Task Queue:** Celery

### Frontend
- **Framework:** React 18
- **State Management:** Redux Toolkit
- **UI Library:** Material-UI (MUI) & TailwindCSS
- **HTTP Client:** Axios
- **Real-time:** Socket.IO Client
- **Charts:** Recharts / Chart.js

---

## 🚀 Quick Start Guide

Follow these steps to get the project running on your local machine.

### Prerequisites
- Python 3.10+
- Node.js 18+
- Git
- `pip` and `npm` package managers

### 1. Clone the Repository
```bash
git clone https://github.com/vishakha2121/speech-multimodal-ai.git
cd speech-multimodal-ai

# Create and activate a virtual environment
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env and add your GEMINI_API_KEY

# Initialize the database
alembic upgrade head

# Navigate to frontend directory
cd ../frontend
npm install

# Create frontend environment file
cp .env.example .env
# Edit .env to point to your backend API

# Terminal 1: Start Backend (from /backend)
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

# Terminal 2: Start Frontend (from /frontend)
npm start