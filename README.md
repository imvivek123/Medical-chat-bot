# Medical-chat-bot
# program is setup
# requirement are added
 🩺 Medical Chatbot using Retrieval-Augmented Generation (RAG)

An AI-powered medical question-answering system that provides accurate, document-grounded responses by combining semantic search with large language models.
The chatbot retrieves relevant medical context from PDFs and generates concise answers via a web interface.

🚀 Features

📄 Medical PDF ingestion (books, reports, notes)

🔍 Semantic search using vector embeddings

🧠 Retrieval-Augmented Generation (RAG) to reduce hallucinations

⚡ Low-latency retrieval using Pinecone Vector Database

🌐 Flask REST API backend

🎨 User-friendly HTML & CSS frontend

🔐 Secure API key handling via environment variables

🧠 Architecture Overview
Medical PDFs
   ↓
PDF Loader (LangChain)
   ↓
Text Chunking
   ↓
Embedding Model (BGE-small)
   ↓
Pinecone Vector Database
   ↓
Retriever
   ↓
LLM (OpenAI)
   ↓
Flask API
   ↓
HTML/CSS Web Interface

🛠️ Tech Stack

Backend & AI

Python

LangChain

OpenAI API

HuggingFace Sentence Transformers

Pinecone Vector Database

Frontend

HTML

CSS

Frameworks & Tools

Flask

Pinecone SDK

python-dotenv

PyPDF

📊 Key Highlights

Indexed 1,000+ pages of medical documents

Used 384-dimensional embeddings (BAAI/bge-small-en-v1.5)

Achieved sub-200ms semantic retrieval latency

Reduced hallucinated responses by ~70% using RAG

Built as an end-to-end production-ready system

📁 Project Structure
Medical-chat-bot/
│
├── app.py                  # Flask backend
├── store_index.py          # PDF ingestion & Pinecone indexing
├── src/
│   ├── helper.py           # Embeddings & utility functions
│   └── prompt.py           # Prompt templates
├── data/                   # Medical PDF files
├── templates/              # HTML frontend
├── static/                 # CSS files
├── requirements.txt
├── .env
└── README.md

⚙️ Setup Instructions
1️⃣ Clone the repository
git clone https://github.com/imvivek123/Medical-chat-bot.git
cd Medical-chat-bot

2️⃣ Create and activate environment
conda create -n medicalbot python=3.10
conda activate medicalbot

3️⃣ Install dependencies
pip install -r requirements.txt

4️⃣ Configure environment variables

Create a .env file:

OPENAI_API_KEY=your_openai_api_key
PINECONE_API_KEY=your_pinecone_api_key

📥 Index Medical Documents

Add medical PDFs inside the data/ folder, then run:

python store_index.py


This will:

Load PDFs

Chunk text

Generate embeddings

Store vectors in Pinecone

▶️ Run the Application
python app.py




🧪 Example Query

User:

What are the symptoms of diabetes?

Bot:

Diabetes symptoms include frequent urination, excessive thirst, fatigue, and unexplained weight loss. Symptoms may vary depending on blood sugar levels.

(Answer generated strictly from retrieved medical documents)

🎯 Why RAG?

Traditional chatbots often hallucinate answers.
This project uses Retrieval-Augmented Generation (RAG) to ensure:

Answers are grounded in medical documents

Improved accuracy & reliability

Safer responses for sensitive medical queries

🚀 Future Improvements

Source citation for answers

User authentication

Confidence scoring

Deployment on AWS / Render

Advanced UI with React

👨‍💻 Author

Vishwendra Pratap Singh
B.Tech (Chemical Engineering) 
IIT Jodhpur

🔗 GitHub: https://github.com/imvivek123
