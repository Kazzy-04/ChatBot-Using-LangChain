# 🤖 RAG Chatbot with LangChain & Google Generative AI

## 📌 Overview

This project implements a **Retrieval-Augmented Generation (RAG) Chatbot** using **LangChain**, **Google Generative AI (Gemma model)**, and **vector embeddings**.

The chatbot is capable of:

* Answering domain-specific questions
* Retrieving relevant knowledge from a custom knowledge base
* Maintaining conversation memory for follow-up queries

---

## ⚙️ Features

✔ RAG-based chatbot (retrieval + generation)
✔ Wikipedia-based knowledge base
✔ Document chunking & embedding
✔ Vector database using ChromaDB
✔ Conversational memory (context-aware responses)
✔ Source citation for answers
✔ Evaluation pipeline
✔ Streamlit app for UI

---

## 🛠️ Tech Stack

* **Python**
* **LangChain**
* **Google Generative AI (Gemma)**
* **HuggingFace Embeddings**
* **Chroma Vector Database**
* **Streamlit**
* **Wikipedia API**

---

## 🔄 Workflow

### 1️⃣ Knowledge Base Creation

* Extracted content from Wikipedia topics:

  * Artificial Intelligence
  * Machine Learning
  * Deep Learning
  * NLP
  * Neural Networks

* Limited content size for efficiency

---

### 2️⃣ Text Chunking

* Used `RecursiveCharacterTextSplitter`
* Chunk size: 500
* Overlap: 50

This improves retrieval accuracy.

---

### 3️⃣ Embeddings & Vector Store

* Embedding Model:

  ```python
  all-MiniLM-L6-v2
  ```

* Stored embeddings in **ChromaDB**

* Enables semantic search

---

### 4️⃣ Model Setup

* LLM: **Google Generative AI (Gemma)**
* Temperature: 0.3 (controlled responses)

---

### 5️⃣ Conversational RAG Chain

* Built using `ConversationalRetrievalChain`
* Includes:

  * Retriever (vector DB)
  * LLM
  * Memory (chat history)

---

### 6️⃣ Memory Handling

* Used `ConversationBufferMemory`
* Enables:

  * Follow-up questions
  * Context-aware answers

---

### 7️⃣ Chatbot Testing

Example queries:

* What is machine learning?
* How is it different from deep learning?
* Give real-world examples

✔ Supports multi-turn conversations

---

### 8️⃣ Evaluation

Tested using sample questions:

* Neural networks
* NLP
* Deep learning applications

Metrics collected:

* Answer length
* Source documents used

---

### 9️⃣ Streamlit Web App

A simple UI is implemented using **Streamlit**:

Features:

* Interactive chatbot interface
* Real-time responses
* Clean UI

---

## 🚀 Getting Started

### 🔧 Installation

```bash
pip install langchain langchain-community langchain-google-genai \
chromadb sentence-transformers streamlit wikipedia
```

---

### 🔑 Setup API Key

```python
os.environ["GOOGLE_API_KEY"] = "your_api_key_here"
```

---

### ▶️ Run Notebook

```bash
jupyter notebook
```

---

### 🌐 Run Streamlit App

```bash
streamlit run app.py
```

---

## 💬 Example Interaction

```
You: What is machine learning?
Bot: Machine learning is a subset of AI that...

You: How is it different from deep learning?
Bot: Deep learning is a subset of ML that uses neural networks...
```

---

## 📊 Project Structure

```
├── Task-4(Chatbot_Lang-chain).ipynb
├── README.md
```

---

## 📌 Future Improvements

* 🔥 Add more diverse knowledge sources (PDFs, APIs)
* ⚡ Use faster vector databases (FAISS)
* 🧠 Improve prompt engineering
* 🌍 Deploy online (Streamlit Cloud / AWS)
* 📈 Add evaluation metrics (BLEU, ROUGE)

---


