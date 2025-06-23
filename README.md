# 🤖 AI Receptionist — Voice-Enabled Generative AI Assistant

**Built during my internship at [Systems Limited](https://www.systemsltd.com/), Pakistan’s largest IT company — this solo project is a voice-interactive AI receptionist powered by Whisper, LangChain, and ElevenLabs.**  

Ask it anything about the company — it listens, understands, and responds in a natural voice, trained on 100+ real webpages scraped from the Systems Limited website.

---

## 📺 Demo

🎥 [Watch the recorded demo](https://drive.google.com/file/d/1JInIiivD3RBrqDqMrg24oT3hcPp_cvXB/view)

---

## 🧠 Why I Built This

Receptionists are often the first point of contact for a business — but most chatbots today are limited to static FAQs and clunky interfaces.

**This project reimagines that role using cutting-edge generative AI:**
- It understands natural spoken language using Whisper (OpenAI)
- It’s trained on real company knowledge using LangChain and FAISS
- It speaks back fluently using ElevenLabs TTS
- It’s adaptable to any company, instantly becoming their voice

> This was my first-ever project in AI/ML, and I completed it solo in just 4 weeks — from idea to deployment-ready prototype.

---

## ✨ Key Features

✅ Voice-to-voice interaction (speak and get a spoken answer)  
✅ Trained on over **100+ pages of company data**  
✅ Real-time transcription + response using LLM  
✅ Web UI built in Streamlit  
✅ Modular and fully open-source

---

## 🧰 Tech Stack

| Component | Tool |
|----------|------|
| Speech to Text | [Whisper](https://github.com/openai/whisper) by OpenAI |
| Vector Store + Retrieval | FAISS + LangChain |
| Text to Speech | [ElevenLabs](https://www.elevenlabs.io/) |
| UI | Streamlit |
| Data Source | Web scraping 100+ pages from [Systems Limited](https://www.systemsltd.com/) |
| Language Model | OpenAI GPT-3.5 via LangChain |

---

## ⚙️ How It Works

1. **Web Scraping**
   - I scraped 100+ pages from the official Systems Limited website
   - Cleaned and concatenated the content into documents
   - Embedded using OpenAI + FAISS for vector search

2. **LangChain + LLM**
   - Integrated LangChain’s `ConversationalRetrievalChain` with GPT-3.5
   - Enabled multi-turn memory with session history

3. **Voice I/O**
   - **Input**: Uses `st_audiorec` + Whisper to transcribe user voice
   - **Output**: ElevenLabs generates natural speech in a custom voice

4. **Frontend**
   - Built a responsive UI in Streamlit with both text and voice options

---

## 💡 Use Cases

- AI-powered Receptionist for corporate websites
- Onboarding assistant for new employees
- Internal HR or IT Helpdesk Q&A bot
- Custom voice bots for product support or marketing

---

## 📁 Project Structure

```bash
ai-receptionist/
├── app/
│   ├── main.py                  # Final Streamlit UI
│   ├── chatbot.py               # Chat logic w/ LangChain
│   ├── audio.py                 # Whisper + ElevenLabs utils
│   ├── st_custom_components/
│   │   └── st_audiorec/
│   │       └── frontend/
│   │           └── build/       # Custom JS audio recorder
│   └── utils/
│       ├── scraper_example.py   # Scraping and preprocessing
│       └── concatenate.py       # Combining + cleaning docs
├── new_faiss_index/
│   ├── index.faiss
│   └── index.pkl
├── Recorded Demo.mp4            # Demo video (optional)
├── requirements.txt
├── .env.example
└── README.md
