# Pinecone VectorDB with OpenAI and LangChain: PDF-based Question Answering System

## Project Overview
This project implements a Question-Answering (QA) System using Pinecone VectorDB, OpenAI, and LangChain. The system reads a set of PDFs stored in a directory, extracts the text, and generates vector embeddings for the text using OpenAI. The vectors are stored in Pinecone VectorDB, where similarity searches are performed based on cosine similarity scores to find the most relevant answers to user queries.

## Features
1. PDF Directory: A directory containing PDFs from which text is extracted.
2. Question-Answer Based System: Supports natural language queries from users, which are answered based on the content extracted from the PDFs.
3. Similarity Search: Uses cosine similarity to rank answers by relevance.
4. Pinecone VectorDB: Efficient storage and retrieval of vector embeddings.
5. OpenAI: For generating embeddings of the PDF content and handling queries.
6. LangChain: Orchestrates the interaction between the vector database and the language model to build a robust QA system.

## Tech Stack
1. Pinecone VectorDB: Vector database for storing and querying vector embeddings.
2. OpenAI API: To generate vector embeddings from text and handle language model queries.
3. LangChain: To streamline the integration between OpenAI, Pinecone, and the search logic.
4. PDF Processing Libraries: (e.g., PyMuPDF, pdfplumber) for extracting text from PDF files.

## Project Workflow
1. PDF Text Extraction: The system scans the PDF directory and extracts the text from each document.
2. Embedding Generation: OpenAI’s embedding models generate vector embeddings for each chunk of text.
3. Vector Storage: The embeddings are stored in Pinecone’s VectorDB.
4. Question Query: A user submits a query, and OpenAI generates a vector embedding for the query.
5. Cosine Similarity Search: The query vector is compared with stored embeddings in Pinecone using cosine similarity to identify relevant content.
6. Answer Extraction: The most relevant chunk of text is returned as the answer to the user’s query.
