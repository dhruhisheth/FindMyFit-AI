# 👗 FindMyFit.AI

FindMyFit.AI is a smart, voice-activated personal stylist that analyzes your outfit and gives stylish, honest, and encouraging feedback — just like talking to your fashionable best friend. Using multimodal AI from GROQ and high-quality speech synthesis from ElevenLabs, this tool helps users look and feel their best with quick, personalized guidance.

---

## 🔥 Features

- 🎤 **Voice Input**: Speak your fashion question with Gradio's built-in microphone
- 🖼️ **Image Upload**: Submit an outfit photo for evaluation
- 🧠 **AI Analysis**: Powered by GROQ’s Whisper and LLaMA-4 for transcription and style intelligence
- 🗣️ **Voice Response**: Replies with expressive audio using ElevenLabs text-to-speech
- 💁‍♀️ **Stylist Personality**: Responds like a warm, encouraging expert — not a robot

---

## 🛠️ Tech Stack

- **Python 3.12+**
- **Gradio** (user interface)
- **GROQ API**: Whisper v3 for speech-to-text, LLaMA-4 Scout for multimodal image+text analysis
- **ElevenLabs API**: for natural voice responses
- **gTTS**: backup voice engine
- **Base64 / PyDub / SpeechRecognition**: audio + image preprocessing

---

## 🚀 Getting Started

#### 1. Clone this repository

```bash
git clone https://github.com/dhruhisheth/FindMyFit-AI.git
cd FindMyFit-AI
```
#### 2. Install dependencies

```bash
pip install -r requirements.txt
```

#### 3. Set up your `.env` file  
Create a `.env` file in the root directory:
```bash
GROQ_API_KEY=your_groq_api_key_here
ELEVENLABS_API_KEY=your_elevenlabs_api_key_here
```  
✅ Never commit this file — it’s already in `gitignore`.

#### 4. Run the application
```bash
python gradio_app.py
```  
This will open a Gradio web interface where you can record your voice, upload your outfit image, and get a voice response from your AI stylist.

---

## 📁 Project Structure
```bash
FindMyFit-AI/
├── gradio_app.py                # Gradio interface and main workflow
├── brain_of_the_file.py        # Handles image + query processing with GROQ LLaMA
├── voice_of_the_user.py        # Audio recording & Whisper transcription
├── voice_of_the_AI.py          # ElevenLabs & gTTS text-to-speech handlers
├── .gitignore
├── README.md
├── Pipfile / requirements.txt
└── .env.example (optional, add your keys)
```
---

## 💡 Example Interaction  

> 🎤 _"Does this outfit work for a summer brunch?"_  
> 🖼️ _(You upload your outfit image)_   
> 🗣️ _"I love the relaxed vibe — to make it even more brunch-perfect, try adding a light hat or woven bag for that airy, effortless look!"_

---

## 🛡️ Security Reminder  
Please keep your `.env` file private. This project uses environment variables to manage sensitive API keys (GROQ and ElevenLabs). The `.env` file is excluded from version control by default.
