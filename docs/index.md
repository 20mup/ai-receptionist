# 🤖 AIVA – AI Voice Assistant for Enterprises

**Built during my internship at [Systems Limited](https://www.systemsltd.com/), AIVA is a fully voice-interactive assistant that allows users to ask questions and receive spoken answers about a company — powered by Whisper, GPT, FAISS, and ElevenLabs.**

---

## 📌 Objective

To create a voice-enabled AI receptionist that could:
- Understand natural spoken language from users
- Search through hundreds of company-specific documents
- Respond with accurate, human-sounding answers
- Be easily adapted to other companies with minimal setup

This project aimed to go beyond static FAQs and deliver a fluid, human-like interaction using generative AI technologies.

---

## 🔧 Technical Breakdown

### 🧠 Knowledge Base

I began by scraping **100+ pages** from the Systems Limited website, including:
- Company history, services, locations, leadership bios
- Whitepapers, news, blog posts, and investor info

These pages were cleaned and chunked using LangChain, then embedded into a **FAISS** vector database using OpenAI embeddings.

### 🗣️ Voice Input + Transcription

The app accepts voice input using a custom Streamlit component built with JavaScript.  
Captured audio is passed to **Whisper**, which returns the full transcription.

### 🤖 Query Answering Logic

The transcription is processed through a **LangChain ConversationalRetrievalChain**, which:
- Retrieves relevant chunks from FAISS
- Pipes them into **OpenAI GPT-3.5** for final response generation
- Maintains conversational memory across turns

### 🔊 Voice Output

Final GPT output is sent to **ElevenLabs**, which converts text into fluent speech using a realistic, professional voice.  
This completes the full **voice-to-voice loop**.

---

## 💻 Technologies Used

| Function           | Tool/Library             |
|--------------------|--------------------------|
| Speech Recognition | Whisper (OpenAI)         |
| LLM Integration    | LangChain + GPT-3.5      |
| Data Storage       | FAISS Vector Index       |
| Text-to-Speech     | ElevenLabs               |
| Web UI             | Streamlit                |
| Data Collection    | Playwright (Scraping)    |

---

## 🎯 Key Features

- Fully voice-interactive — speak and receive answers
- 100% customizable — retrainable on any company’s knowledge base
- Supports multi-turn memory (context-aware follow-ups)
- Natural, human-like speech via ElevenLabs
- Streamlit frontend with fallback text input

---

## 💡 Challenges Faced

- **Chunking web content** effectively for vector search without noise
- Balancing response length vs clarity from GPT
- Handling minor transcription errors from Whisper
- Setting up robust .env variable handling for secure API keys
- Making sure latency stayed low despite multiple APIs in use

---

## 🧠 What I Learned

- How to design modular LangChain pipelines (retrieval → memory → generation)
- Deploying real-time Whisper + TTS in a desktop-grade app
- Writing maintainable Python backend code in a short sprint
- Importance of consistent formatting + chunking for retrieval quality

---

## 📽️ Demo

Watch the full demo recording here:  
🎥 [Click to View AIVA in Action](https://drive.google.com/file/d/1JInIiivD3RBrqDqMrg24oT3hcPp_cvXB/view)

---

## 📂 GitHub + Assets

- [🔗 GitHub Repository](https://github.com/20mup/ai-receptionist)
- [🎨 Interface Preview](../assets/images/aiva/interface.png)
- [📸 Hero Banner](../assets/images/aiva/hero.png)

---

> _“AIVA gave me my first real taste of what’s possible with multimodal AI — and I built it from scratch in 4 weeks.”_
