🦜 LangChain Learning Journey

A personal learning repo documenting my day-by-day progress in LangChain with Python — building toward a fully functional Jarvis AI Assistant 🤖


👨‍💻 About This Repo
This repository contains my notes, code, and experiments as I learn LangChain from scratch. I follow the LangChain Tamil Tutorial series by Computer Lab Tamil and document everything here for reference.
Goal: Build a voice-to-voice AI Assistant (Jarvis) using:

🦜 LangChain
🤖 Ollama (Local LLM)
🎤 Whisper (Speech to Text)
🔊 Text to Speech


📚 Progress
DayTopicNotebookStatusDay 1LLM Intro + PromptTemplate + LCEL Basics01_llm_prompt_basics.ipynb✅ DoneDay 2Text Completion vs Chat Models + Model Parameters02_text_completion_vs_chat_models.ipynb✅ DoneDay 3Runnables, Passthrough, Lambda & ParallelComing soon...🔜Day 4Output ParsersComing soon...🔜Day 5ChainsComing soon...🔜Day 6Chatbot with MemoryComing soon...🔜Day 7RAGComing soon...🔜Day 8Agents & ToolsComing soon...🔜

🗂️ Repo Structure
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

⚙️ Setup & Installation
1. Clone the repo
bashgit clone https://github.com/yourusername/langchain-learning.git
cd langchain-learning
2. Create virtual environment
bashpython -m venv .venv
.venv\Scripts\activate      # Windows
source .venv/bin/activate   # Mac/Linux
3. Install dependencies
bashpip install -r requirements.txt
4. Setup .env file
Create a .env file in the root folder:
GOOGLE_API_KEY=your_google_api_key_here
OPENAI_API_KEY=your_openai_api_key_here
GROQ_API_KEY=your_groq_api_key_here
5. Setup Ollama (for local LLM)
bash# Install Ollama from https://ollama.com
ollama pull tinyllama   # lightweight model for learning
ollama serve

🧰 Tech Stack
ToolPurpose🦜 LangChainAI application framework⚡ Groq APIFree & fast cloud LLM (works in India!)🤖 OllamaRun LLMs locally🧠 Google GeminiCloud LLM🐍 Python 3.11+Programming language📓 Jupyter NotebookLearning & experimentation🔐 python-dotenvAPI key management

📖 Key Concepts Learned
Day 1 — LLM + PromptTemplate + LCEL

LLM = The brain of the app (GPT, Gemini, Ollama, Groq)
PromptTemplate = Reusable text templates with {variables}
input_variables = Registers blank spaces in the template
LCEL = Connect components with | pipe operator
chain.invoke() = Run the chain with input
res.content = Get the text output from AIMessage

Day 2 — Text Completion vs Chat Models

PromptTemplate = Simple string, no roles
ChatPromptTemplate = Conversation style with system & human roles ✅
temperature=0 = Focused, factual answers
temperature=1 = Creative, random answers
max_tokens = Limit the response length
Text Completion Model = Old way → returns plain string
Chat Model = Modern way → returns AIMessage, use .content ✅


🐛 Common Errors & Fixes
ErrorCauseFixValidationError: api_keyWrong parameter nameUse google_api_key=429 RESOURCE_EXHAUSTEDGemini free tier quota exceededSwitch to Groq API (free in India!)404 NOT_FOUNDModel version mismatchRun genai.list_models() to check available modelsOllama slow (5 mins)Running on CPU onlyUse Groq API instead for learningModuleNotFoundErrorPackage not installedRun pip install <package-name>SyntaxErrorCopied markdown text into code cellCopy only the Python code!

💡 Pro Tips

For India users → Google Gemini free tier has limit=0. Use Groq API instead — it's free and super fast! ⚡
For slow PC → Skip Ollama during learning, use Groq API. Switch to Ollama when building the final project.
Always use ChatModel + ChatPromptTemplate for modern LangChain apps!


🙏 Credits

Tutorial: LangChain Tamil Series by Praveen KJ
LangChain Official Docs
LangChain Official Course
Groq Console — Free LLM API


📬 Connect With Me

LinkedIn: https://www.linkedin.com/in/mohammed-yasin-a-o1/
GitHub: https://github.com/yasinmass/


⭐ Star this repo if you find it helpful!
