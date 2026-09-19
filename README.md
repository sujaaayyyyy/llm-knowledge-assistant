# Smart AI Knowledge Assistant

A document-based AI Knowledge Assistant built using Large Language Models (LLMs), Retrieval-Augmented Generation (RAG), LangChain, Google Gemini, and FAISS.

Developed as a hands-on project during a 3-day Add-on Course on Large Language Models conducted by Evolve Robotics at Vimal Jyothi Engineering College.

## Overview

The Smart AI Knowledge Assistant allows users to ask questions about information contained in PDF documents. It retrieves relevant content from the documents and uses Google Gemini to generate context-aware responses.

## Features

- Ask questions about uploaded PDF documents
- Extract and process PDF content
- Split documents into manageable text chunks
- Generate embeddings for document content
- Store and search embeddings using FAISS
- Retrieve relevant document information using RAG
- Generate answers using Google Gemini
- System date and time tool

## Architecture

```text
User
  |
  v
Gemini LLM
  |
  v
Tool Decision
  |
  +---- document_search
  |          |
  |          v
  |       Retriever
  |          |
  |          v
  |        FAISS
  |          |
  |          v
  |      PDF Documents
  |
  +---- system_datetime
             |
             v
       Current Date/Time
  |
  v
Gemini LLM
  |
  v
Final Answer
RAG Pipeline
PDF Documents
      |
      v
PyPDFLoader
      |
      v
Text Splitting
      |
      v
Gemini Embeddings
      |
      v
FAISS Vector Store
      |
      v
Retriever
      |
      v
Relevant Chunks
      |
      v
Google Gemini
      |
      v
Generated Answer
Tech Stack
Python
LangChain
Google Gemini
FAISS
PyPDF
Python-dotenv
Retrieval-Augmented Generation (RAG)
Vector Embeddings
Project Structure
llm-knowledge-assistant/
|
├── main.py
├── rag.py
├── tools.py
├── rrrr.txt
├── requirements.txt
├── README.md
├── .gitignore
└── documents/
Installation

Clone the repository:

git clone https://github.com/sujaaayyyyy/llm-knowledge-assistant.git
cd llm-knowledge-assistant

Create a virtual environment:

python -m venv venv

Activate it on Windows:

venv\Scripts\activate

Install the dependencies:

pip install -r requirements.txt
API Key Setup

Create a .env file in the project root:

GOOGLE_API_KEY=your_api_key_here

Do not share or upload your API key.

Adding Documents

Create a documents folder in the project directory and place your PDF files inside it.

documents/
└── your_document.pdf
Running the Application

Run:

python main.py

Then ask questions related to the information contained in your uploaded documents.

Example:

You: What is machine learning?

AI: [Answer generated using information retrieved from the PDF]
Key Components
Component	Purpose
Google Gemini	Language model and embeddings
LangChain	LLM application framework
FAISS	Vector storage and similarity search
PyPDF	PDF document processing
Retriever	Retrieves relevant document chunks
RAG	Provides relevant document context to the LLM
Tools	Handles document search and system date/time
Files
File	Purpose
main.py	Main AI assistant and conversation handling
rag.py	PDF loading, text chunking, embeddings and FAISS
tools.py	Custom tools used by the assistant
requirements.txt	Python dependencies
documents/	Local PDF knowledge base
.env	Google Gemini API key
Learning Outcomes

Through this project, I gained practical experience with:

Large Language Models (LLMs)
Retrieval-Augmented Generation (RAG)
Vector embeddings
Vector databases and similarity search
LangChain
Google Gemini
PDF document processing
Building document-based AI applications
Future Improvements
Persistent FAISS index
Web-based user interface
Conversation memory
Source and page citations
Additional AI tools
Support for multiple document formats
Acknowledgement

This project was developed as part of a 3-day Add-on Course on Large Language Models conducted by Evolve Robotics at Vimal Jyothi Engineering College.


### Step 2 — Save

Press:

**Ctrl + S**

Then check how it looks in VS Code's Markdown preview:

**Ctrl + Shift + V**

You should now see proper emojis/text instead of:

```text
ðŸ§
â†“
â”œ