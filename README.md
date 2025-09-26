

# 📘 RAG Local LLM with LangChain

This project demonstrates a **Retrieval-Augmented Generation (RAG) pipeline** built with **LangChain**.
It uses PDFs as the knowledge base, stores embeddings in **Postgres + PGVector**, and generates **context-aware answers** with **Google Gemini LLM**.

---

## 🚀 Features

* **📄 Load and split documents from PDFs**
* **🧠 Generate embeddings** with HuggingFace (`all-MiniLM-L6-v2`)
* **🗄️ Store and search embeddings** in Postgres using PGVector
* **🔍 Retrieve the most relevant chunks** for any query
* **🤖 Answer queries** using Google Gemini LLM with context

---

## 📂 Project Structure

```
Rag_local_LLM/
 ├── main_code.ipynb       # Jupyter notebook with full pipeline
 ├── data/
 │    └── book.pdf         # Example knowledge base (replace with your documents)
 ├── requirements.txt      # Dependencies
 └── README.md             # Project documentation
```

---

## ⚙️ Setup

### 1️⃣ Clone the repo & create environment

```bash
git clone https://github.com/vasee-garan/Rag.git
cd Rag_local_LLM

# Create virtual environment
python -m venv rag
source rag/bin/activate   # On Windows: rag\Scripts\activate
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

**requirements.txt:**

```
langchain
langchain-community
langchain-huggingface
langchain-postgres
langchain-google-genai
psycopg2-binary
python-dotenv
```

### 3️⃣ Setup Postgres with PGVector```

### 4️⃣ Configure API Keys

Create a `.env` file in the project root:

```
GOOGLE_API_KEY=your_google_gemini_api_key
```

---

## ▶️ Usage

### 1️⃣ Run Jupyter Notebook

```bash
jupyter notebook main_code.ipynb
```

## 📌 Notes

* Make sure **Postgres with PGVector** is running before executing the notebook.
* Replace `book.pdf` with your own dataset.
* HuggingFace MiniLM is lightweight and works well on low-RAM systems.
* **Gemini LLM** requires an API key.

---

