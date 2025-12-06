# Specification Document

## Book Title
"The Beginner's Guide to AI Engineering with Docusaurus & RAG"

## Audience
Beginners to intermediate developers.

## Table of Contents
1. Introduction to AI Engineering  
2. Setting Up Docusaurus  
3. Writing Your First Chapter  
4. What Is RAG?  
5. Embeddings Explained  
6. Qdrant Setup  
7. FastAPI Backend  
8. Frontend Chat UI  
9. Deploying the Chatbot  
10. Best Practices  

## Docusaurus Structure
/docs  
  - intro.md  
  - chapter-1.md  
  - chapter-2.md  

## Chatbot Tech Stack
- Backend: FastAPI  
- Database: Neon Serverless Postgres  
- Vector Store: Qdrant Cloud Free Tier  
- AI SDK: OpenAI Agents / ChatKit  

## RAG Flow
1. Convert docs into embeddings  
2. Store embeddings in Qdrant  
3. On query, retrieve nearest matches  
4. Pass matches to LLM  
5. Generate answer based only on retrieved context  

## Naming Conventions
- All files lowercase  
- Hyphens for multiple words (e.g., chapter-one.md)  
