# QA-Bot-that-Leverages-the-LangChain-and-LLM-to-Answer-Questions-from-Loaded-Document

This repository contains the code for a project developed as part of the course **"Generative AI Engineering with LLMs Specialization"**.  

The project demonstrates how to build an intelligent question-answering (QA) bot capable of quickly and accurately answering queries based on content from large PDF documents. By combining modern AI technologies like LangChain, Large Language Models (LLMs), and Gradio, this bot provides an efficient alternative to manually searching through extensive document libraries.  

---

## Features  

- **Document Loading:** Automatically read content from PDF files.  
- **Text Splitting:** Divide large documents into manageable chunks for better processing.  
- **Embeddings:** Convert text into vector representations for semantic similarity searches.  
- **Vector Databases:** Store and retrieve vectorized text efficiently.  
- **Question Answering:** Leverage LLMs to provide accurate answers based on document content.  
- **Interactive UI:** Seamlessly interact with the bot using a Gradio-based interface.  

---

## Learning Objectives  

This project consolidates multiple AI components and techniques, helping you:  

1. Combine document loaders, text splitters, embedding models, and vector databases to construct a functional QA bot.  
2. Use LangChain and LLMs to retrieve and answer questions from large document libraries.  
3. Build a user-friendly interface using Gradio for real-time interaction with the bot.  

---

## Technologies Used  

- **LangChain**: For handling the pipeline of operations.  
- **Large Language Models (LLMs)**: For understanding and answering questions.  
- **Gradio**: To create an intuitive user interface.  
- **Python Libraries**: Including PyPDF2 (or similar) for PDF handling, FAISS for vector search, and Hugging Face transformers for embeddings.  

---

# How It Works

## Load Documents
Upload PDFs to the bot via the Gradio interface.

## Process Text
The documents are split into smaller sections for efficient handling.

## Embed Text
Text is converted into vector embeddings for similarity search.

## Store in Vector Database
The embeddings are stored in a vector database for quick retrieval.

## Query and Answer
Enter your question, and the bot retrieves the most relevant text sections and generates an answer using an LLM.
