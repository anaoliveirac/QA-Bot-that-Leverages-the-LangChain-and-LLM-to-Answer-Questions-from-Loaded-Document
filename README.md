# QA-Bot-that-Leverages-the-LangChain-and-LLM-to-Answer-Questions-from-Loaded-Document

This repository contains the code for a project developed as part of the course **"Generative AI Engineering with LLMs Specialization"**.  

The project demonstrates how to build an intelligent question-answering (QA) bot capable of quickly and accurately answering queries based on content from large PDF documents. By combining modern AI technologies like LangChain, Large Language Models (LLMs), and Gradio, this bot provides an efficient alternative to manually searching through extensive document libraries.  

---

## Features

- **PDF Document Processing**: Automatically reads and processes PDF files using PyPDFLoader
- **Intelligent Text Splitting**: Divides documents into manageable chunks using RecursiveCharacterTextSplitter
- **Advanced Embeddings**: Utilizes IBM WatsonX's slate-125m-english-rtrvr model for text embeddings
- **Vector Storage**: Implements Chroma vector store for efficient similarity search
- **Large Language Model Integration**: Powered by Mixtral-8x7B Instruct v0.1 through WatsonX.ai
- **Interactive Interface**: User-friendly Gradio web interface for document upload and querying

## Technologies Used

- **IBM WatsonX.ai**: For both LLM inference and text embeddings
  - LLM: mistralai/mixtral-8x7b-instruct-v01
  - Embeddings: ibm/slate-125m-english-rtrvr
- **LangChain**: For orchestrating the RAG pipeline
- **Chroma**: Vector database for storing and retrieving embeddings
- **Gradio**: Web interface framework
- **PyPDF**: PDF document processing

## How It Works

1. **Document Upload**: Users upload PDF files through the Gradio interface
2. **Document Processing**:
   - The PDF is loaded using PyPDFLoader
   - Text is split into chunks of 1000 characters with 50-character overlap
   - Chunks are converted to embeddings using WatsonX's slate-125m model
   - Embeddings are stored in a Chroma vector database
3. **Query Processing**:
   - User questions are processed by the retrieval system
   - Relevant document chunks are retrieved from the vector store
   - Mixtral-8x7B generates answers based on the retrieved context

## System Architecture

The system uses a RetrievalQA chain with the following components:
- Document Loader: PyPDFLoader
- Text Splitter: RecursiveCharacterTextSplitter (chunk_size=1000, overlap=50)
- Embeddings: WatsonX Embeddings (slate-125m-english-rtrvr)
- Vector Store: Chroma
- LLM: WatsonX (Mixtral-8x7B Instruct)
- Interface: Gradio web UI

## Usage

The application runs on port 7861 and can be accessed through a web browser. Users can:
1. Upload a PDF document using the file upload interface
2. Enter questions about the document content
3. Receive AI-generated answers based on the document context

## Technical Configuration

- **LLM Parameters**:
  - Max new tokens: 256
  - Temperature: 0.5
- **Embedding Parameters**:
  - Truncate input tokens: 3
  - Returns input text with embeddings

## Requirements

- IBM WatsonX.ai access
- Python with required libraries:
  - ibm_watsonx_ai
  - langchain
  - langchain_ibm
  - gradio
  - chromadb
