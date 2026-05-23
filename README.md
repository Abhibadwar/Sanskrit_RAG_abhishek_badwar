# Sanskrit RAG System

## Project Overview

This project is a Sanskrit Retrieval-Augmented Generation (RAG) System built using:

- LangChain
- HuggingFace
- ChromaDB
- TinyLlama
- Multilingual Embeddings

The system answers user questions from Sanskrit documents only.

---

# Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming Language |
| LangChain | RAG Pipeline |
| Transformers | LLM Inference |
| TinyLlama | Text Generation |
| ChromaDB | Vector Database |
| HuggingFace Embeddings | Semantic Embeddings |

---

# Project Workflow

Document  
↓  
Chunking  
↓  
Embeddings  
↓  
Vector Database  
↓  
Retriever  
↓  
Prompt  
↓  
LLM  
↓  
Final Answer

---

# Installation

Create virtual environment:

```bash
python -m venv venv
```

Activate environment:

```bash
venv\Scripts\activate
```

Install requirements:

```bash
pip install -r requirements.txt
```

---

# Requirements

```txt
transformers
langchain
langchain-community
langchain-huggingface
sentence-transformers
chromadb
docx2txt
```

---

# Dataset

Input file:

```txt
Rag-docs.docx
```

Contains:
- Sanskrit stories

---

# Embedding Model

```python
sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2
```

Purpose:
- Semantic retrieval
- Multilingual understanding
- Sanskrit support

---

# LLM Used

```python
TinyLlama/TinyLlama-1.1B-Chat-v1.0
```

Purpose:
- Generate answers from retrieved context

---

# Chunking Strategy

```python
chunk_size=500
chunk_overlap=50
```

Purpose:
- Better retrieval
- Context continuity

---

# Retriever Settings

```python
search_type="similarity"
k=3
```

Purpose:
- Retrieve top 3 relevant chunks

---

# Prompt Engineering

The system uses strict prompts:

```txt
Answer ONLY from the given context.
```

Purpose:
- Reduce hallucination
- Improve factual accuracy

---


# Output Files

| File | Purpose |
|---|---|
| accuracy.xlsx | Accuracy Evaluation |
| Sanskrit_RAG_Technical_Report.pdf | Technical Documentation |

---

# Running the Project

```bash
python app.py
```

---

# Example Question

```txt
Who was the servant in the story मूर्खभृत्यस्य?
```

---

# Advantages

- Simple RAG pipeline
- CPU compatible
- Easy to understand
- Good for Sanskrit QA systems
- Reduces hallucinations

---

# Limitations

- TinyLlama has limited reasoning capability
- Accuracy depends on retrieval quality
- Small context window


---

# Conclusion

This project demonstrates a complete Sanskrit RAG system using modern NLP techniques such as semantic retrieval, vector databases, multilingual embeddings, and transformer-based language models.
