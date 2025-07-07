# 🤖 AIVA — AI Voice Assistant for Enterprises

> Voice-powered receptionist built with Whisper, LangChain, FAISS, and ElevenLabs — built during my internship at Systems Limited.

AIVA (AI Voice Assistant) is a voice-interactive AI receptionist that can answer company-specific questions by listening to your voice, retrieving accurate info from real webpages, and responding with natural speech.

---

## 📺 Demo

[![Watch the demo](https://img.youtube.com/vi/_fyLJ0vlOlo/maxresdefault.jpg)](https://youtu.be/_fyLJ0vlOlo)

---

## 🚀 Why I Built This

During my internship at Systems Limited, I saw an opportunity to bring generative AI to a real business use case: reception and onboarding. I pitched AIVA as a solo project to my manager and VP — and after 4 weeks of development, I presented it to 60+ employees and the President of IT.

---

## ✨ Features

- 🎙️ Voice-to-voice interaction (ask a question, hear a reply)
- 📚 Trained on 100+ webpages scraped from systemsltd.com
- 🧠 LangChain + GPT-3.5 for accurate retrieval and context
- 🗣️ ElevenLabs voice output with natural tone
- 💻 Built in Streamlit — no setup, just run and speak

---

## 🧰 Tech Stack

| Purpose            | Tools Used                        |
|-------------------|------------------------------------|
| Speech-to-Text     | [Whisper](https://github.com/openai/whisper) (OpenAI) |
| Knowledge Retrieval | FAISS + LangChain                |
| Text-to-Speech     | [ElevenLabs](https://www.elevenlabs.io) |
| Interface          | Streamlit                         |
| Language Model     | GPT-3.5 (via LangChain)           |
| Web Scraping       | BeautifulSoup                     |

---

## 🧠 How It Works

1. **Scrape company content** → chunk into documents  
2. **Embed content using OpenAI embeddings + FAISS index**  
3. **Capture voice via Whisper**, convert to text  
4. **Query LangChain’s retrieval chain** → generate response  
5. **Use ElevenLabs** to speak the result out loud  
6. **Streamlit UI** glues the entire experience together

---

## 📁 Project Structure

```bash
ai-receptionist/
├── app/
│   ├── main.py                # Streamlit UI
│   ├── chatbot.py             # LangChain logic
│   ├── audio.py               # Whisper + ElevenLabs integration
│   ├── st_custom_components/  # Custom JS audio recorder
│   └── utils/
│       ├── scraper_example.py
│       └── concatenate.py
├── new_faiss_index/           # Saved FAISS vector index
├── requirements.txt
├── .env.example
└── README.md
```

---

## 📝 Setup Instructions

1. **Clone the repo**
```bash
git clone https://github.com/20mup/ai-receptionist
cd ai-receptionist
```

2. **Create a virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Add your API keys to `.env`**
```
OPENAI_API_KEY=your-openai-key
ELEVENLABS_API_KEY=your-elevenlabs-key
```

5. **Run the app**
```bash
streamlit run app/main.py
```

---

## 🤝 Credits

Developed by [Mousa Pirzada](https://www.linkedin.com/in/mousa-pirzada/)  
Internship: Systems Limited — Cloud & Infrastructure Division  
Special thanks to my mentors and VP for trusting me with this initiative.

---

> _From static FAQs to fluent conversations — AIVA makes companies sound smarter._
