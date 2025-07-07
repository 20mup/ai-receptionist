# 🧠 AIVA: AI Voice Assistant for Enterprises  
**Built during my internship at Systems Limited**

---

## 🔍 Project Background

In Summer 2023, I joined **Systems Limited**, Pakistan’s largest IT company, as an intern in the **Cloud & Infrastructure Division**. My internship was initially structured as a traditional corporate rotation — visiting departments, learning what they do, and preparing a final presentation.

I completed all of that in just under a week.

While most interns would stop there, I wasn’t satisfied with just learning. I wanted to **create something lasting**. With encouragement from my manager and VP, I pitched an original idea: to build a **voice-based AI receptionist** using the emerging power of LLMs and audio models like Whisper and ElevenLabs — a project that would go on to change how the company saw AI.

---

## 💡 The Spark Behind AIVA

While exploring different departments, I noticed a gap: **Systems Limited had no intelligent assistant to help onboard guests or employees**. There was someone who could give directions — but nothing more.

At the same time, I was learning about cutting-edge tools like:
- **Whisper** for speech-to-text
- **LangChain** for chaining LLM-based operations
- **FAISS** for vector-based knowledge retrieval
- **ElevenLabs** for high-quality text-to-speech

These tools were still **very new** — LangChain had only launched a few months earlier — and I saw an opportunity to integrate them into a **real, working solution**.

That weekend, I built the plan for AIVA — an AI Voice Assistant trained on company data that could answer spoken questions like:
> “What does Systems Limited do in the healthcare sector?”

---

## 🏗️ Development Process

### ✅ 1. Web Scraping & Data Curation  
- Scraped **100+ public pages** from Systems Limited’s official website using BeautifulSoup.
- Cleaned and concatenated them into vector-chunked documents.
- Created a **FAISS index** from OpenAI embeddings to enable fast, relevant retrieval.

### ✅ 2. LangChain-Powered Chatbot  
- Used `ConversationalRetrievalChain` for context-aware conversations.
- Integrated session memory to support **multi-turn interactions**.

### ✅ 3. Voice Input & Output  
- Whisper converted microphone input to clean, accurate text.
- ElevenLabs TTS returned a **clear, expressive voice** answer using a female assistant-style voice.

### ✅ 4. Frontend & Deployment  
- Built a responsive **Streamlit** interface with voice and text input modes.
- Delivered a working prototype with modular backend logic and production-ready front-end flow.

---

## 📣 Presentation & Impact

- Held a **live Zoom demo** for over **60 employees** across departments.
- Received direct feedback and questions from multiple engineering teams.
- Personally invited to demo AIVA 1-on-1 with the **President of the IT Division**.
- Offered a **full-time role** on the spot to continue developing the tool — but turned it down to complete my degree.

> “This is the direction we want to go in — and you just did it solo.”  
> — *President, Systems Limited IT Division*

---

## 🌟 What Made AIVA Different

- **Voice-first interface** instead of static web chat  
- **Live knowledge updates** via web scraping and retraining  
- **End-to-end pipeline**, built by one person in 4 weeks

---

## 🧠 Lessons & Reflections

- Initiating a technical project from scratch inside a corporate structure is hard — but worth it.
- LLMs are only as useful as the context you feed them. Proper chunking + embedding is everything.
- Simple interfaces (Streamlit + audio) can outperform flashy dashboards when solving a clear problem.

---

## 📎 Learn More

- [🔗 GitHub Repository](https://github.com/20mup/ai-receptionist)
- [🎥 Watch Demo](https://youtu.be/_fyLJ0vlOlo)
- [🌐 Back to Portfolio](https://20mup.github.io)

---

> _Built to leave a mark, not just complete a task._  
> — Mousa Pirzada
