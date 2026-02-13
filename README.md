<div align="center">

# 🦜🔗 LangChain Document Loaders Lab

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/LangChain-Document%20Loaders-00A67E)](https://github.com/langchain-ai/langchain)
[![HuggingFace](https://img.shields.io/badge/LLM-HuggingFace-FFCA28?logo=huggingface&logoColor=black)](https://huggingface.co/)
[![Status](https://img.shields.io/badge/Status-Active-2EA44F)]()

### Developed by **[Ghulam Muhammad]**
*Building the foundation for Agentic AI in 2026*

---
</div>

This repository documents my hands-on exploration of **LangChain Document Loaders** and how they ingest structured and unstructured data for LLM-powered pipelines.

The goal of this project is to deeply understand how different data sources are transformed into `Document` objects and how they can be integrated into LCEL chains for summarization and question-answering workflows.

---

## 📂 Repository Structure

```
.
├── books/
│   └── ML book PDFs
├── cricket.txt
├── Social_Network_Ads.csv
├── dl-curriculum.pdf
├── csv_loader.py
├── directory_loader.py
├── pdf_loader.py
├── text_loader.py
├── webbase_loader.py
└── requirements.txt
```

---

## 🔍 Covered Loaders

This lab explores the following loaders from:

`langchain_community.document_loaders`

### 1️⃣ CSVLoader

Loads structured tabular data from CSV files.

* Converts each row into a `Document`
* Useful for analytics, RAG over datasets, structured QA

File: `csv_loader.py`

---

### 2️⃣ PyPDFLoader

Loads and splits PDF files page-by-page.

* Extracts page content
* Preserves metadata (page number, source)

File: `pdf_loader.py`

---

### 3️⃣ DirectoryLoader

Loads multiple files from a directory using a specified loader class.

* Batch ingestion
* Useful for document corpora

File: `directory_loader.py`

---

### 4️⃣ TextLoader + LLM Chain

Loads plain text and connects it to an LLM pipeline for summarization.

* Demonstrates LCEL (`prompt | model | parser`)
* Uses HuggingFace endpoint for inference

File: `text_loader.py`

---

### 5️⃣ WebBaseLoader + QA Chain

Loads webpage content and performs question-answering over scraped text.

* Demonstrates web ingestion
* Demonstrates contextual LLM querying

File: `webbase_loader.py`

---

## 🧠 Concepts Explored

* Document abstraction in LangChain
* `Document.page_content`
* `Document.metadata`
* `load()` vs `lazy_load()`
* LCEL chaining
* Structured vs Unstructured ingestion
* Web scraping considerations
* LLM integration with HuggingFace endpoints

---

## 🏗 Why This Repository Exists

Understanding data ingestion is the **foundation of RAG systems**.

Before building:

* Vector databases
* Retrieval pipelines
* Agents

You must understand:

> How raw data becomes structured `Document` objects.

This repository is part of my deeper exploration into:

* Agentic AI systems
* Retrieval-Augmented Generation (RAG)
* Production-grade LLM pipelines

---

## ⚙️ Requirements

```bash
pip install -r requirements.txt
```

---

## 🔐 Environment Variables

Create a `.env` file:

```
HUGGINGFACEHUB_API_TOKEN=your_token_here
USER_AGENT=Mozilla/5.0
```

---

## 🚀 Future Extensions

* Add Text Splitters
* Add Embeddings
* Add Vector Store integration
* Convert pipelines to fully runnable graphs
* Add RAG example.
