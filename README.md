# Retrieval-Augmented Generation (RAG) demo with LangChain

Demoing Retrieval-Augmented Generation through simple Jupyterlab python progam. This is a simple yet complete RAG pipeline built with local components so no OpenAI keys, no API calls, and no cloud dependencies needed.

## Functionality

- Loads a text file example.txt (for example a Wikipedia page pasted to example.txt)
- Splits it into overlapping chunks using LangChain
- Embeds the chunks locally using `all-MiniLM-L6-v2`
- Stores embeddings in a FAISS vector index
- Uses `flan-t5-base` to answer questions based on retrieved chunks

## Technologies

- LangChain
- HuggingFace
- Transformers
- SentenceTransformers
- FAISS
- JupyterLab

## Installation

Create a clean virtual environment:

```python3 -m venv venv```
```source venv/bin/activate```

Install required packages:

```pip install langchain langchain-community langchain-huggingface sentence-transformers faiss-cpu transformers ipywidgets jupyter```

## How to use 

Open rag_demo.ipynb in JupyterLab
Paste a wikipedia page text into example.txt

Execute the cells:

- Load the text file
- Split and embed chunks
- Create the retriever and the QA chain
- Ask your questions

Example:

ask("What is *title of your text* known for?")
