# LangChain PDF Question-Answering Bot

A simple Retrieval-Augmented Generation (RAG) application built using LangChain. This project allows users to ask questions about a PDF document and receive answers generated only from the document's content instead of the model's general knowledge.

The main goal of this project was to learn how a complete RAG pipeline works using LangChain, FAISS, embeddings, and a Large Language Model.

---

## Features

- Load PDF documents using PyPDFLoader
- Split documents into manageable text chunks
- Generate embeddings using Sentence Transformers
- Store embeddings in a FAISS vector database
- Retrieve relevant document chunks based on user queries
- Generate answers using GPT-4.1-mini through the GitHub Models API
- Restrict responses to information available in the uploaded document
- Built using LangChain Expression Language (LCEL)

---

## Tech Stack

- Python
- LangChain
- FAISS
- Sentence Transformers
- GPT-4.1-mini
- GitHub Models API
- PyPDFLoader
- RecursiveCharacterTextSplitter

---

## Project Workflow

1. Load the PDF document.
2. Split the document into smaller chunks.
3. Generate embeddings for every chunk.
4. Store the embeddings inside FAISS.
5. Convert the user question into an embedding.
6. Retrieve the most relevant document chunks.
7. Send the retrieved context along with the question to GPT-4.1-mini.
8. Return an answer based only on the retrieved content.

---

## Project Structure

```
.
├── langchain_pdf_qa.ipynb
├── solar_system.pdf
├── solar_system_index/
├── .env
├── requirements.txt
└── README.md
```

---

## Installation

Clone the repository.

```bash
git clone https://github.com/yourusername/langchain-pdf-qa.git
cd langchain-pdf-qa
```

Install the required packages.

```bash
pip install -r requirements.txt
```

---

## Environment Variables

Create a `.env` file.

```text
GITHUB_TOKEN=your_github_models_api_key
```

---

## Example

**Question**

```
What is Jupiter known for?
```

**Answer**

```
Jupiter is the largest planet in the Solar System. It is famous for the Great Red Spot, a giant storm, and has more than 95 known moons.
```

---

## What I Learned

While building this project I gained practical experience with:

- LangChain
- Retrieval-Augmented Generation (RAG)
- Vector databases
- Embeddings
- Semantic search
- Prompt templates
- LCEL chains
- Document-based question answering

---

## Future Improvements

- Support multiple PDF uploads
- Build a Streamlit interface
- Display source page numbers
- Add chat history
- Support larger documents
- Use different embedding models

---

## License

This project is created for learning purposes.
