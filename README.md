<div align="center">
<img src="https://img.shields.io/badge/🐾_Veterinary_Advisor_Bot-Local_LLM_Powered-blue?style=for-the-badge&labelColor=1a1a2e&color=16213e" alt="Project Banner" width="600"/>

<br/>

<img src="https://img.shields.io/badge/Gemma_4-Ollama-orange?style=flat-square&logo=google&logoColor=white" alt="Gemma 4"/>
<img src="https://img.shields.io/badge/Python-3.9+-blue?style=flat-square&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/Streamlit-Web_UI-red?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit"/>
<img src="https://img.shields.io/badge/Click-CLI-green?style=flat-square&logo=gnu-bash&logoColor=white" alt="Click CLI"/>
<img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="License"/>

<br/><br/>

<strong>Part of <a href="https://github.com/kennedyraju55/90-local-llm-projects">90 Local LLM Projects</a> collection</strong>

</div>

<br/>
# 🐾 Veterinary Advisor Bot

![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![LLM](https://img.shields.io/badge/LLM-Ollama%2FGemma4-orange.svg)
![UI](https://img.shields.io/badge/UI-Streamlit-red.svg)

> AI-powered pet health advice chatbot with medical disclaimers, symptom tracking, and breed-specific guidance.

## ✨ Features

- **Pet Profile Storage** — Save and manage multiple pet profiles
- **Symptom Analysis** — Get possible causes and urgency levels
- **Symptom History** — Track symptoms over time per pet
- **Breed-Specific Advice** — Tailored care tips for specific breeds
- **Nutrition Guidance** — Diet and feeding recommendations
- **8 Pet Types** — Dog, cat, bird, fish, rabbit, hamster, reptile, and more
- **Emergency Detection** — Flags urgent symptoms needing immediate vet attention
- **Medical Disclaimers** — Always reminds users to consult a real veterinarian
- **Streamlit Web UI** — Full-featured browser interface

## 📦 Installation

```bash
pip install -r requirements.txt
```

## 🚀 CLI Usage

```bash
# Interactive mode with pet profile setup
python -m vet_advisor.cli chat-cmd

# Quick start with pet info
python -m vet_advisor.cli chat-cmd --pet-type dog --name "Buddy" --breed "Labrador"

# List saved pets
python -m vet_advisor.cli list-pets
```

### Chat Commands

| Command | Description |
|---------|-------------|
| `/symptoms <desc>` | Analyze specific symptoms |
| `/breed` | Get breed-specific advice |
| `/nutrition` | Get nutrition advice |
| `/history` | View symptom history |
| `quit` | Exit the app |

## 🌐 Web UI

```bash
streamlit run src/vet_advisor/web_ui.py
```

The web UI provides:
- 💬 Interactive health consultation chat
- 🐾 Pet profile management with sidebar
- 🩺 Symptom analysis and history tracking
- 🐕 Breed-specific and nutrition advice

## 🧪 Running Tests

```bash
python -m pytest tests/ -v
```

## 📸 Screenshots

<div align="center">
<table>
<tr>
<td><img src="https://via.placeholder.com/400x250/1a1a2e/e94560?text=CLI+Interface" alt="CLI Interface"/></td>
<td><img src="https://via.placeholder.com/400x250/16213e/e94560?text=Web+UI" alt="Web UI"/></td>
</tr>
<tr>
<td align="center"><em>CLI Interface</em></td>
<td align="center"><em>Streamlit Web UI</em></td>
</tr>
</table>
</div>

## 📁 Project Structure

```
07-veterinary-advisor-bot/
├── src/
│   └── vet_advisor/
│       ├── __init__.py       # Package metadata
│       ├── core.py           # Core business logic
│       ├── cli.py            # Click CLI interface
│       ├── web_ui.py         # Streamlit web interface
│       ├── config.py         # Configuration management
│       └── utils.py          # Helper utilities
├── tests/
│   ├── __init__.py
│   ├── test_core.py          # Core logic tests
│   └── test_cli.py           # CLI tests
├── config.yaml               # Default configuration
├── setup.py                  # Package setup
├── requirements.txt          # Dependencies
├── Makefile                  # Common commands
├── .env.example              # Example environment variables
└── README.md                 # This file
```
