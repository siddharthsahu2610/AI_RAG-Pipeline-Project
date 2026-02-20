# AI_RAG-Pipeline-Project
Retrieval-Augmented Generation (RAG) is a technique that improves AI accuracy by fetching relevant data from external sources (documents, databases) before generating a response, effectively grounding Large Language Models (LLMs) in real-time, trustworthy information. It reduces hallucinations and eliminates the need for frequent retraining.

# AI Study Assistant (RAG-Powered)
An intelligent study assistant built using Retrieval-Augmented Generation (RAG) and Groq LLM API, capable of answering questions from uploaded documents, generating summaries, and creating revision questions. 

This project implements a production-style RAG pipeline that allows users to:
--> Upload study PDFs
--> Ask contextual questions
--> Generate document summaries
--> Create practice questions
--> View retrieved context chunks

System Design

1️⃣ Document Processing - Extract text from PDF, Split into manageable chunks, Convert chunks into embeddings

2️⃣ Vector Storage - Store embeddings in FAISS index, Enables fast similarity search

3️⃣ Retrieval - Convert user query into embedding, Retrieve top-k similar chunks, Pass chunks to LLM as context

4️⃣ Generation (Groq API) - Construct prompt with: Retrieved context, User query, Groq LLM generates grounded answer
