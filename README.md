🔍 RAG Pipeline with LangChain, FAISS & Groq/OpenAI LLMs
An end-to-end Retrieval-Augmented Generation (RAG) system that combines the power of vector search and large language models (LLMs) to answer domain-specific questions from your documents. Designed for scalable, modular, and production-ready use in real-world applications like resume screening, internal Q&A, financial report analysis, and more.
🚀 Features
📚 Document Ingestion: Load PDFs, text, or CSVs and chunk them into embeddings.

🧠 Semantic Search: Retrieve relevant chunks using FAISS vector store.

🤖 Contextual Answering: Augment queries with retrieved documents and generate responses via Groq's Llama3 / OpenAI GPT using LangChain.

🔁 Chat History Memory: Optional support for conversational memory.

🧱 Modular Codebase: Built for easy swapping of LLMs, vector DBs, and embedding models.

🧠 How RAG Works (Simple Diagram)

           ┌───────────────┐
           │ User Question │
           └──────┬────────┘
                  ↓
         ┌──────────────────┐
         │ Retrieve Top-K   │
         │ chunks using FAISS│
         └──────┬───────────┘
                ↓
       ┌─────────────────────┐
       │ Combine query + docs│
       └──────┬──────────────┘
              ↓
   ┌────────────────────────────┐
   │ Send to LLM (Groq/OpenAI) │
   └──────────┬────────────────┘
              ↓
        🔁 Response to user
