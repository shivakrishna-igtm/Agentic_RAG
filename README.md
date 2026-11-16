Agentic RAG — Interactive Learning Guide
A browser-based, beginner-friendly guide to understanding Agentic Retrieval-Augmented Generation (Agentic RAG), from document chunking and semantic search to multi-agent routing, answer evaluation, and web-search fallback.
Overview
Traditional RAG retrieves context from documents before generating an answer. Agentic RAG adds decision-making and verification: agents can choose between private PDF knowledge and web search, evaluate whether an answer is relevant and grounded, and use a fallback when a check fails.

This repository contains an interactive HTML learning guide explaining that architecture through diagrams, analogies, example code, exercises, and quizzes.
What's inside
- Interactive route map: Follow sample questions through PDF retrieval, web search, answer grading, hallucination grading, and final response generation.
- RAG fundamentals: Document loading, chunking, overlap, embeddings, vector storage, and top-k retrieval.
- Interactive labs: Experiment with chunk sizes and overlap; explore an illustrative semantic-search map.
- Five-agent architecture: Router, Retriever, Answer Grader, Hallucination Grader, and Answer Generator.
- Implementation walkthrough: CrewAI agents and tasks, config.py, llms.py, tools.py, and main.py.
- Model and tool choices: DeepSeek through OpenRouter, a fast RAG model via Groq, BAAI embeddings, ChromaDB, and web search.
- Practical learning: Local model setup, troubleshooting, real-world use cases, exercises, a quiz, and a glossary.
Architecture
User question
     |
     v
   Router
   /    \
  v      v
PDF RAG  Web search
  \      /
   v    v
  Retriever
     |
     v
 Answer Grader
     |
     v
Hallucination Grader
     |
     v
 Answer Generator
     |
     v
 Final answer
If a validation check fails, the guide illustrates a web-search fallback before producing a final answer.
View the guide
1. Download or clone this repository.
2. Open Agentic_RAG_Guide.html in a modern browser.
3. Use the chapter navigation, interactive diagrams, sliders, and quiz to explore the concepts.
No API keys or Python installation are needed to read and interact with the HTML guide. Running the separate Python Agentic RAG example described inside the guide requires the dependencies and credentials explained in its setup chapter.
Learning path
1. Understand why RAG exists and how traditional RAG works.
2. Explore failure modes such as irrelevant retrieval and hallucinations.
3. Learn the five-agent architecture and how tools are selected.
4. Walk through a sample question from routing to final answer.
5. Study the Python project structure and code examples.
6. Practice with the interactive labs, exercises, and quiz.
Technologies discussed
AI orchestration: CrewAI, DeepSeek, OpenRouter, Groq
Retrieval: ChromaDB, BAAI/bge-small-en-v1.5, PDF search, semantic embeddings
Programming and presentation: Python, HTML, CSS, JavaScript
This repository is an educational guide, not by itself a deployed Agentic RAG backend. The Python implementation is explained in the guide; the uploaded artifact is an HTML learning resource.
