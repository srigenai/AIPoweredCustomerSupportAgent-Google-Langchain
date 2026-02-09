📌 Overview

This project implements an AI-powered customer support agent that automatically processes incoming customer emails from start to finish.
The agent classifies emails by urgency and topic, searches relevant documentation, drafts customer responses, escalates complex issues to human agents, and schedules follow-ups when required.

The system is built using Python, LangChain, and Google Gemini, with a strong emphasis on:

Correctness

Clear decision logic

Human-in-the-loop safety

Real-world applicability

🎯 Objectives

Automatically handle customer support emails

Reduce manual workload for support teams

Ensure urgent and complex cases are escalated appropriately

Provide consistent, professional responses
🧠 Core Capabilities

✔ Read and understand customer emails
✔ Classify urgency (Low, Medium, High)
✔ Classify topic (Account, Billing, Bug, Feature Request, Technical Issue)
✔ Retrieve relevant documentation using vector search
✔ Generate customer-ready email responses
✔ Escalate high-risk or unresolved issues to humans
✔ Schedule follow-ups when needed

🏗️ Architecture Overview
Incoming Email
      ↓
LLM-Based Classifier (LangChain + Gemini)
      ↓
Knowledge Base Retrieval (Vector Search)
      ↓
Response Generator (LLM)
      ↓
Escalation Logic (Deterministic Rules)
      ↓
Follow-Up Scheduler
      ↓
Final Decision (Auto-Reply or Escalation)

📁 Project Structure

ai_support_agent/
├── agent.py              # Main orchestrator
├── llm.py                # Google Gemini LLM configuration
├── classifier.py         # Urgency & topic classification
├── knowledge_base.py     # Vector-based documentation search
├── responder.py          # Customer response generation
├── escalation.py         # Escalation decision logic
├── followup.py           # Follow-up scheduling
├── sample_emails.py      # Example test inputs
├── README.md             # Project documentation
└── .env                  # API keys (not committed)

⚙️ Technology Stack

Python 3.10+

LangChain

Google Gemini (via langchain-google-genai)

FAISS (vector search)

Google Generative AI Embeddings

🔑 Setup Instructions
1️⃣ Install Dependencies
pip install langchain langchain-google-genai langchain-community google-generativeai python-dotenv faiss-cpu

