# 🦜 LangChain Learning Journey

> A personal learning repo documenting my day-by-day progress in LangChain with Python — building toward a fully functional **Jarvis AI Assistant** 🤖

---

## 👨‍💻 About This Repo

This repository contains my notes, code, and experiments as I learn LangChain from scratch. I follow the **LangChain Tamil Tutorial series** by [Computer Lab Tamil](https://www.youtube.com/@ComputerLabTamil) and document everything here for reference.

**Goal:** Build a voice-to-voice AI Assistant (Jarvis) using:
- 🦜 LangChain
- 🤖 Ollama (Local LLM)
- 🎤 Whisper (Speech to Text)
- 🔊 Text to Speech

---

## 📚 Progress

| Day | Topic | Notebook | Status |
|-----|-------|----------|--------|
| Day 1 | LLM Intro + PromptTemplate + LCEL Basics | [01_llm_prompt_basics.ipynb](./01_llm_prompt_basics.ipynb) | ✅ Done |
| Day 2 | Text Completion vs Chat Models + Model Parameters | [02_text_completion_vs_chat_models.ipynb](./02_text_completion_vs_chat_models.ipynb) | ✅ Done |
| Day 3 | Runnables, Passthrough, Lambda & Parallel | Coming soon... | 🔜 |
| Day 4 | Output Parsers | Coming soon... | 🔜 |
| Day 5 | Chains | Coming soon... | 🔜 |
| Day 6 | Chatbot with Memory | Coming soon... | 🔜 |
| Day 7 | RAG | Coming soon... | 🔜 |
| Day 8 | Agents & Tools | Coming soon... | 🔜 |

---

## 🗂️ Repo Structure

```
langchain-learning/
│
├── README.md
├── .env                                        # API keys (not pushed to GitHub)
├── .gitignore
├── requirements.txt
│
├── 01_llm_prompt_basics.ipynb                  # Day 1 - LLM + PromptTemplate
├── 02_text_completion_vs_chat_models.ipynb     # Day 2 - Text Completion vs Chat Models
└── ...                                         # More coming daily!
```

---

## ⚙️ Setup & Installation

### 1. Clone the repo
```bash
git clone https://github.com/yourusername/langchain-learning.git
cd langchain-learning
```

### 2. Create virtual environment
```bash
python -m venv .venv
.venv\Scripts\activate      # Windows
source .venv/bin/activate   # Mac/Linux
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Setup `.env` file
Create a `.env` file in the root folder:
```
GOOGLE_API_KEY=your_google_api_key_here
OPENAI_API_KEY=your_openai_api_key_here
GROQ_API_KEY=your_groq_api_key_here
```

### 5. Setup Ollama (for local LLM)
```bash
# Install Ollama from https://ollama.com
ollama pull tinyllama   # lightweight model for learning
ollama serve
```

---

## 🧰 Tech Stack

| Tool | Purpose |
|------|---------|
| 🦜 LangChain | AI application framework |
| ⚡ Groq API | Free & fast cloud LLM (works in India!) |
| 🤖 Ollama | Run LLMs locally |
| 🧠 Google Gemini | Cloud LLM |
| 🐍 Python 3.11+ | Programming language |
| 📓 Jupyter Notebook | Learning & experimentation |
| 🔐 python-dotenv | API key management |

---

## 📖 Key Concepts Learned

### Day 1 — LLM + PromptTemplate + LCEL
- **LLM** = The brain of the app (GPT, Gemini, Ollama, Groq)
- **PromptTemplate** = Reusable text templates with `{variables}`
- **input_variables** = Registers blank spaces in the template
- **LCEL** = Connect components with `|` pipe operator
- **chain.invoke()** = Run the chain with input
- **res.content** = Get the text output from AIMessage

### Day 2 — Text Completion vs Chat Models
- **PromptTemplate** = Simple string, no roles
- **ChatPromptTemplate** = Conversation style with `system` & `human` roles ✅
- **temperature=0** = Focused, factual answers
- **temperature=1** = Creative, random answers
- **max_tokens** = Limit the response length
- **Text Completion Model** = Old way → returns plain string
- **Chat Model** = Modern way → returns AIMessage, use `.content` ✅

---

## 🐛 Common Errors & Fixes

| Error | Cause | Fix |
|-------|-------|-----|
| `ValidationError: api_key` | Wrong parameter name | Use `google_api_key=` |
| `429 RESOURCE_EXHAUSTED` | Gemini free tier quota exceeded | Switch to **Groq API** (free in India!) |
| `404 NOT_FOUND` | Model version mismatch | Run `genai.list_models()` to check available models |
| `Ollama slow (5 mins)` | Running on CPU only | Use Groq API instead for learning |
| `ModuleNotFoundError` | Package not installed | Run `pip install <package-name>` |
| `SyntaxError` | Copied markdown text into code cell | Copy only the Python code! |

---

## 💡 Pro Tips

- **For India users** → Google Gemini free tier has `limit=0`. Use **Groq API** instead — it's free and super fast! ⚡
- **For slow PC** → Skip Ollama during learning, use Groq API. Switch to Ollama when building the final project.
- **Always use** `ChatModel` + `ChatPromptTemplate` for modern LangChain apps!

---

## 🙏 Credits

- Tutorial: [LangChain Tamil Series](https://www.youtube.com/@ComputerLabTamil) by **Praveen KJ**
- [LangChain Official Docs](https://docs.langchain.com)
- [LangChain Official Course](https://academy.langchain.com)
- [Groq Console](https://console.groq.com) — Free LLM API

---

## 📬 Connect With Me

- LinkedIn: https://www.linkedin.com/in/mohammed-yasin-a-o1/
- GitHub: https://github.com/yasinmass/

---

⭐ **Star this repo if you find it helpful!**
