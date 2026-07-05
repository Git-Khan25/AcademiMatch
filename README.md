# AcademiMatch-CLI

An AI-powered Research Matching Chatbot built using LangGraph, LangChain, ChromaDB, OpenAI, Tavily, and Semantic Scholar.
AcademiMatch-CLI is an intelligent research matching assistant that helps students discover faculty members aligned with their research interests and enables professors to identify collaboration opportunities using Retrieval-Augmented Generation (RAG), vector search, and live academic trend analysis.

The chatbot operates entirely through a terminal interface and uses a LangGraph workflow to orchestrate retrieval, recommendation, project suggestion, collaboration analysis, and human-in-the-loop email approval.

---

## Team

Team Name: "Ai For Good"

Members:-
```
- Rachamalla Sai Arnav Goud - 25881A05DW -> Team Lead
- Mohammed Faroz Khan - 25881A05CQ
- Vishvas Polepaka - 25881A05EN
- Kunduru Bharath Reddy - 25881A05CL
```
---
## Features

- Faculty matching using Hybrid RAG
- ChromaDB vector search
- OpenAI embeddings
- Tavily web search integration
- Semantic Scholar paper retrieval
- Student and Professor modes
- LangGraph workflow
- Human-in-the-loop email confirmation
- Project recommendation engine
- Research gap analysis
- Collaboration recommendation
- Faculty workload analysis
- ASCII terminal interface

---
## Tech Stack

Create a table.
```
Technology	      Purpose
------------------------------------------------
Python	          Backend
LangChain	        RAG Pipeline
LangGraph	        Workflow
ChromaDB	        Vector Database
OpenAI	          LLM + Embeddings
Tavily	          Live Search
Semantic          Scholar	Academic Papers
dotenv	          Environment Variables
```
---

## Project Architecture
```
AcademiMatch
        │
        ▼
User Query
        │
        ▼
Router
        │
 ┌──────┴─────────┐
 │                │
Student        Professor
 │                │
 ▼                ▼
RAG          Paper Search
 │                │
 ▼                ▼
Projects     Collaboration
 │                │
 └──────┬─────────┘
        ▼
Email Generator
        ▼
Human Approval
        ▼
Reporter
```
---

## Folder Structure

```
research-chatbot/
│
├── data/
│   ├── faculty/
│   └── fallback_papers.json
│
├── eval/
│   ├── run_eval.py
│   └── test_queries.json
│
├── src/
│   ├── graph.py
│   ├── router.py
│   ├── rag_retriever.py
│   ├── faculty_loader.py
│   ├── detail_retriever.py
│   ├── paper_searcher.py
│   ├── gap_analyzer.py
│   ├── collab_matcher.py
│   ├── project_suggester.py
│   ├── workload_checker.py
│   ├── email_generator.py
│   ├── email_approval.py
│   ├── human_validator.py
│   ├── reporter.py
│   └── state.py
│
├── demo.py
├── main.py
├── requirements.txt
└── README.md
```
---
## Installation

```
git clone <repository>

cd Research_matching_agent-main

pip install -r requirements.txt
```
---
## Environment Variables
```
OPENAI_API_KEY=
TAVILY_API_KEY=
```
---

## Running the Project
```
python main.py

python demo.py
```
---

## Workflow
```
Start
   │
   ▼
Load Faculty Database
   │
   ▼
Create ChromaDB
   │
   ▼
Receive User Query
   │
   ▼
Router
   │
   ▼
Hybrid Retrieval
   │
   ▼
Faculty Ranking
   │
   ▼
Project / Papers / Collaboration
   │
   ▼
Email Approval
   │
   ▼
Report
```
---

## Example Conversation
```
User:
Who works on NLP?

↓

Top Matches

1. Dr. Priya Sharma
Match Score: 91%

2. Dr. Rahul Mehta
Match Score: 84%

3. Dr. Sneha Rao
Match Score: 80%

↓

User:
Tell me about Dr. Priya Sharma

↓

Research areas
Recent papers
Current projects

↓

User:
Email this professor

↓

Draft Generated

↓

YES

↓

[SIMULATED] Email Sent
```
---
## Future Improvements
- Web interface
- PDF paper parsing
- Gmail API integration
- Citation graph visualization
- Multi-university faculty database
- User authentication
- Research proposal generation
---
