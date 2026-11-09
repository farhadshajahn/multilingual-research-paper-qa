# Multilingual Research Paper QA System

An end-to-end **Retrieval-Augmented Generation (RAG)** application that enables users to ask questions about research papers in **English, Hindi, and Kannada**.

The system retrieves relevant information from uploaded PDF research papers and generates concise, context-aware answers using multilingual embeddings and a lightweight language model.

## Features

- 📄 Upload and process research papers in PDF format
- 🌐 Multilingual question answering in English, Hindi, and Kannada
- 🔍 Semantic search using multilingual embeddings
- ⚡ Fast similarity retrieval using FAISS
- 🤖 Context-aware answer generation using FLAN-T5
- 🔄 Translation fallback for multilingual responses
- 💬 Interactive web interface built with Gradio

## System Architecture

1. **PDF Processing:** Extracts text from research papers using `pypdf`.
2. **Text Chunking:** Cleans and divides extracted text into sentence-based chunks using NLTK.
3. **Embedding Generation:** Converts text chunks into dense vector representations using `intfloat/multilingual-e5-base`.
4. **Vector Indexing:** Stores embeddings in FAISS for efficient similarity search.
5. **Query Retrieval:** Embeds user questions and retrieves relevant document chunks.
6. **Answer Generation:** Uses `google/flan-t5-small` to generate concise answers based on retrieved context.
7. **Translation Fallback:** Translates responses when the generated answer does not match the requested language.
8. **User Interface:** Provides an interactive PDF upload and question-answering interface using Gradio.

## Tech Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| PDF Extraction | pypdf |
| Text Processing | NLTK |
| Embedding Model | multilingual-e5-base |
| Vector Database | FAISS |
| Language Model | FLAN-T5 Small |
| UI Framework | Gradio |
| NLP / ML | Hugging Face Transformers |

## Supported Languages

- English
- Hindi
- Kannada

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/multilingual-research-paper-qa.git
cd multilingual-research-paper-qa
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Usage

Run the application:

```bash
python app.py
```

Open the Gradio interface in your browser.

1. Upload a research paper in PDF format.
2. Wait for document processing and indexing.
3. Enter a question in English, Hindi, or Kannada.
4. View the retrieved context and generated answer.

## Project Structure

```text
multilingual-research-paper-qa/
│
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
│
├── src/
│   ├── document_loader.py
│   ├── text_processing.py
│   ├── embeddings.py
│   ├── retrieval.py
│   ├── qa_pipeline.py
│   └── translation.py
│
└── assets/
    └── screenshots/
```

*Note: Adjust this structure to match the actual files in your project.*

## Models

- Embedding Model: `intfloat/multilingual-e5-base`
- Generation Model: `google/flan-t5-small`

These models are loaded from their respective model repositories.

## Future Improvements

- Support for additional Indian languages
- Improved answer faithfulness and retrieval accuracy
- Support for multiple research papers simultaneously
- Citation-aware answers with page references
- Deployment as a public web application

## Author

**Farhad Shajahan**

Artificial Intelligence and Machine Learning

P.A. College of Engineering, Mangaluru

---

If you find this project useful, consider giving the repository a ⭐.

