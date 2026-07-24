# 💬 Conversational RAG Chatbot using LangChain, Groq & ChromaDB

A simple **Conversational Question & Answer (Q&A) Chatbot** built using **LangChain**, **Groq LLM**, **Hugging Face Embeddings**, and **Chroma Vector Database**. The chatbot retrieves relevant information from a webpage using **Retrival-Augmented Generation (RAG)** and maintains **conversation history**, allowing users to ask follow-up questions naturally.

---

## 🚀 Features

- 🤖 Conversational AI powered by **Groq Llama 3.1**
- 📄 Web page ingestion using **WebBaseLoader**
- ✂️ Automatic document chunking
- 🧠 Semantic search using **Hugging Face Embeddings**
- 🗄️ Vector storage with **ChromaDB**
- 🔍 Retrieval-Augmented Generation (RAG)
- 💬 Conversation history support
- 🔄 History-aware question reformulation
- ⚡ Fast and lightweight implementation using LangChain

---

## 🛠️ Tech Stack

- Python
- LangChain
- Groq API
- Hugging Face Embeddings
- ChromaDB
- BeautifulSoup
- LangChain Community
- Jupyter Notebook

---

## 📂 Project Workflow

```
Web Page
    │
    ▼
WebBaseLoader
    │
    ▼
Document Splitting
(RecursiveCharacterTextSplitter)
    │
    ▼
Hugging Face Embeddings
    │
    ▼
Chroma Vector Database
    │
    ▼
Retriever
    │
    ▼
History Aware Retriever
    │
    ▼
Prompt Template
    │
    ▼
Groq Llama 3.1
    │
    ▼
Answer
```

---

## 📁 Project Structure

```
7-CONVERSATIONCHATBOT/
│
├── chatbot.ipynb
├── requirements.txt
├── .env
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd 7-CONVERSATIONCHATBOT
```

### 2. Create a virtual environment

```bash
conda create -n langchain python=3.11
conda activate langchain
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file.

```env
GROQ_API_KEY=your_groq_api_key
HF_TOKEN=your_huggingface_token
USER_AGENT=LangChain-RAG-Chatbot
```

---

## ▶️ How It Works

### Step 1
Load a web page using **WebBaseLoader**.

### Step 2
Split the documents into smaller chunks using:

- RecursiveCharacterTextSplitter

### Step 3
Generate embeddings using:

- HuggingFaceEmbeddings
- Model: `all-MiniLM-L6-v2`

### Step 4
Store the embeddings inside **ChromaDB**.

### Step 5
Retrieve the most relevant chunks based on the user's query.

### Step 6
Generate answers using **Groq's Llama 3.1** model.

### Step 7
Maintain conversation history using:

- `HumanMessage`
- `AIMessage`
- `MessagesPlaceholder`
- `create_history_aware_retriever`

This allows the chatbot to understand follow-up questions such as:

> User: What is Self-Reflection?

> User: Tell me more about it.

without requiring the user to repeat the original question.

---

## 📌 Example Conversation

```
User:
What is Self-Reflection?

Assistant:
Self-reflection is the process of examining one's thoughts,
actions, and experiences to gain a better understanding of
oneself.

User:
Tell me more about it.

Assistant:
Self-reflection helps individuals evaluate past experiences,
learn from mistakes, improve decision-making, and develop
personally and professionally.
```

---

## 🧠 Concepts Used

- LangChain
- Retrieval-Augmented Generation (RAG)
- Chroma Vector Database
- Semantic Search
- Embeddings
- Prompt Engineering
- Conversation Memory
- History-Aware Retrieval
- Groq LLM Integration

---

## 📦 Future Improvements

- Streamlit UI
- PDF Question Answering
- Multi-document Retrieval
- Source Citations
- Persistent Chroma Database
- Chat History Storage
- Voice Input
- Multi-user Sessions

---

## 👨‍💻 Author

**Madhav Manoj**

Built as part of my **LangChain & Generative AI learning journey**, exploring Conversational AI, Retrieval-Augmented Generation (RAG), and LLM application development.
