# 🍽️ GoodFoods: Agentic AI for Restaurant Discovery

A localized, autonomous AI Agent designed for the **Coimbatore market**. This system leverages LLM reasoning to interpret natural language requests, navigate regional dining datasets, and manage table reservations via a custom API backend.

---

## 🚀 The Core "Agentic" Innovation
Unlike a standard chatbot, this project implements a **Reasoning-Action (ReAct) Loop**.

* **Tool Calling:** The agent autonomously determines when it needs external data and triggers Python functions to query the backend.
* **Hybrid Fulfillment:** Designed for the real-world regional market, the agent provides verified landmarks and direct-contact data for establishments that lack digital booking APIs.
* **Zero-Trust Validation:** Custom logic intercepts "AI Hallucinations" (like fake phone numbers or names) before they ever reach the database.

---

## 🛠️ Tech Stack
* **Brain:** Gemini 2.5 Flash 
* **Backend:** FastAPI, Uvicorn
* **Validation:** Pydantic (Type Safety)
* **Data Storage:** Persistent JSON-based Flat File System
* **Tools:** Python, Requests, Logging, Regex

---

## 📂 Project Structure
```plaintext
├── agent/
│   ├── conversation_engine.py  # The "Brain" (LLM Orchestration)
│   ├── prompt_library.py       # System personas & tool definitions
│   └── toolkit.py              # Function logic for the agent
├── data/
│   ├── service_api.py          # FastAPI Backend & Business Logic
│   ├── restaurant_list.json    # Coimbatore Regional Dataset
│   └── bookings_list.json      # Persistent Reservation Logs
├── requirements.txt            # Dependency list
└── start.py                    # Unified entry point
