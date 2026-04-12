# 🐾 Veterinary Advisor Bot

![Python 3.11+](https://img.shields.io/badge/Python-3.11%2B-3776AB?logo=python&logoColor=white)
![License MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Local LLM](https://img.shields.io/badge/LLM-Gemma%204-FF6F00?logo=google&logoColor=white)
![Privacy First](https://img.shields.io/badge/Privacy-First-blueviolet?logo=lock&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-Powered-black?logo=ollama&logoColor=white)

**AI-powered pet health guidance — symptom checking, breed-specific advice, nutrition tips, and care reminders, all running locally with Gemma 4.**

> **Disclaimer:** This bot provides general informational guidance only. It is NOT a substitute for professional veterinary care. Always consult a licensed veterinarian for your pet's health concerns.

```
+---------------------------------------------------------+
|               VETERINARY ADVISOR BOT                    |
|                                                         |
|  +----------+    +---------------+    +--------------+  |
|  | Pet Owner |--->|  CLI / Web UI |--->|  Vet Advisor |  |
|  | (You!)    |<---|  (Rich /      |<---|  Core        |  |
|  +----------+    |  Streamlit)   |    +------+-------+  |
|                  +---------------+           |          |
|  +----------+                                v          |
|  | Pet       |    +---------------+    +--------------+  |
|  | Profiles  |<-->| Symptom       |--->|  Ollama API  |  |
|  | (JSON)    |    | Checker &     |    |  (Gemma 4)   |  |
|  +----------+    | Breed Advisor |    |  :11434      |  |
|                  +-------+-------+    +--------------+  |
|  +----------+            |                              |
|  | Symptom   |<----------+                              |
|  | History   |    + Medical Disclaimer                  |
|  | (JSON)    |    + Urgency Assessment                  |
|  +----------+    + Nutrition Advice                     |
+---------------------------------------------------------+
```

## Features

- **Symptom Checker** — Describe symptoms and get possible causes ranked by likelihood with urgency levels
- **Emergency Detection** — Flags critical symptoms (breathing difficulty, seizures, poisoning) with urgent-care guidance
- **Breed-Specific Advice** — Health predispositions, grooming, exercise, and temperament by breed
- **Nutrition Guidance** — Diet recommendations, portion sizes, foods to avoid, and supplements
- **Pet Profiles** — Store multiple pets with type, breed, age, and weight for personalized advice
- **Symptom History** — Log and review symptoms over time to spot patterns
- **8 Pet Types** — Dogs, cats, birds, fish, rabbits, hamsters, reptiles, and more
- **Medical Disclaimers** — Every response includes responsible AI disclaimers
- **Web UI + CLI** — Streamlit dashboard for browsing or Rich terminal for quick lookups
- **100% Local & Private** — Your pet's health data never leaves your machine

## Quick Start

### Prerequisites

| Requirement | Version |
|-------------|---------|
| Python      | 3.11+   |
| Ollama      | latest  |
| Gemma 4     | via Ollama |

### Install & Run

```bash
# 1. Clone the repository
git clone https://github.com/kennedyraju55/veterinary-advisor-bot.git
cd veterinary-advisor-bot

# 2. Install dependencies
pip install -r requirements.txt

# 3. Start Ollama and pull Gemma 4
ollama serve &
ollama pull gemma4

# 4a. Launch the Web UI
streamlit run src/vet_advisor/web_ui.py

# 4b. Or use the CLI
python -m vet_advisor.cli check --pet-type dog --breed "Golden Retriever" --symptoms "limping on front leg"
```

### Docker

```bash
docker-compose up
# Web UI at http://localhost:8501
```

## Tech Stack

| Layer        | Technology                          |
|-------------|--------------------------------------|
| LLM          | Gemma 4 via Ollama                  |
| Backend      | Python 3.11, Click CLI              |
| Web UI       | Streamlit                           |
| API          | FastAPI / Uvicorn                   |
| Terminal UI  | Rich (panels, tables, progress)     |
| Config       | PyYAML                              |
| Testing      | pytest, pytest-cov                  |
| Containers   | Docker, Docker Compose              |

## Project Structure

```
veterinary-advisor-bot/
├── src/vet_advisor/
│   ├── core.py         # Symptom checker, breed advice, nutrition
│   ├── cli.py          # Click CLI with Rich output
│   ├── web_ui.py       # Streamlit web dashboard
│   ├── api.py          # FastAPI REST endpoints
│   ├── config.py       # YAML configuration loader
│   └── utils.py        # LLM client helpers & utilities
├── common/
│   └── llm_client.py   # Shared Ollama/Gemma 4 client
├── tests/
│   ├── test_core.py    # Unit tests for core logic
│   └── test_cli.py     # CLI integration tests
├── config.yaml         # Pet types, storage paths, UI config
├── requirements.txt    # Python dependencies
├── Dockerfile          # Multi-stage Docker build
├── docker-compose.yml  # Full stack with Ollama
├── Makefile            # Dev shortcuts (install, test, run)
└── setup.py            # Package setup with entry points
```

## Author

**Nrk Raju Guthikonda**
Senior Software Engineer @ Microsoft — Copilot Search Infrastructure

- GitHub: [kennedyraju55](https://github.com/kennedyraju55)
- Dev.to: [kennedyraju55](https://dev.to/kennedyraju55)
- LinkedIn: [nrk-raju-guthikonda](https://linkedin.com/in/nrk-raju-guthikonda-504066a8/)

---

<p align="center">Built with Gemma 4 — part of a 90+ local LLM project portfolio</p>
