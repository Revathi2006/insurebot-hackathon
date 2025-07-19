

# 🛡️ InsureBot - Insurance Query Chatbot with Knowledge Base

InsureBot is an intelligent insurance chatbot developed to assist users with insurance-related queries such as due payments, policy status, company info, and general knowledge like "What is term insurance?". The system uses Retrieval-Augmented Generation (RAG) with Mistral-7B-Instruct (via OpenRouter API) and a custom knowledge base (`scripts.txt`) to respond accurately and naturally.

> This was a group project by **Revathi S.**, **Rattish Kumar S.S**, and **Harini S.**
> 
> The **implementation, design, coding, and deployment was leaded  by Revathi S.**

---

## 💡 Features

- 🔁 Hybrid Chatbot:
  - Responds to known user queries from knowledge base (`scripts.txt`)
  - Falls back to general insurance Q&A using the **Mistral model via OpenRouter**
- 🔍 RAG-based retrieval system using cosine similarity
- 🌐 REST API powered by **Flask**
- 🔊 Voice support for both input and output
- 📜 Scripted questions for FAQ-like guidance
- 📁 Multi-folder modular structure (`kb` for RAG logic, `backend` for Flask app)
- 🌍 Deployable on **Render** with `.env` key management

---

## 🛠️ Tech Stack

| Layer       | Tools/Libs                             |
|-------------|----------------------------------------|
| Backend     | Flask, Python                          |
| Retrieval   | Sklearn (TF-IDF), Cosine Similarity    |
| LLM Model   | Mistral-7B-Instruct via OpenRouter API |
| Environment | Python `dotenv`                        |
| Deployment  | Render, GitHub                         |
| Others      | Flask-CORS, JSON, HTML, JavaScript     |

---

## 📁 Folder Structure

├── backend/

│ ├── app.py # Main Flask app

│ ├── chat_handler.py # Main logic for chatbot

│ ├── rag_retriever.py # Vector search using TF-IDF + cosine similarity

│ ├── .env # API key and model

│ └── requirements.txt # Python dependencies

│
├── kb/

│ └── scripts.txt # Predefined script for the knowledge base

│
├── .gitignore # Ignores .env and pycache

└── README.md # You're reading it!


---

## 🔐 .env File (do not push)

```env
OPENROUTER_API_KEY=your_openrouter_api_key_here
OPENROUTER_MODEL=mistral
```

## Output:

<img width="852" height="860" alt="Screenshot 2025-07-19 214549" src="https://github.com/user-attachments/assets/ef02ca12-657e-4824-ac2d-31de1129d1ce" />

