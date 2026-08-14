# 🤖 Pixotic AI Assistant

<p align="center">
  <strong>Your Personal AI Assistant</strong>
</p>

<p align="center">
  🤖 Gemini AI &nbsp; • &nbsp;
  🧠 Memory &nbsp; • &nbsp;
  📚 RAG &nbsp; • &nbsp;
  🎬 Media &nbsp; • &nbsp;
  📱 Telegram
</p>

---

## 🎬 Pixotic Introduction

<p align="center">
  <a href="./pixoticintro.mp4">
    <img
      src="https://dummyimage.com/1000x560/111111/ffffff&text=▶+WATCH+PIXOTIC+INTRODUCTION"
      alt="Watch Pixotic Introduction"
      width="900"
    />
  </a>
</p>

<p align="center">
  <strong>▶️ Click the preview above to watch the Pixotic introduction</strong>
</p>

---

## ✨ About Pixotic

**Pixotic** is a personal AI assistant built to go beyond a traditional
chatbot.

It combines AI conversation, personal memory, document understanding,
RAG-based retrieval and Telegram interaction into one assistant.

The goal of Pixotic is to create a personal AI companion that can
understand conversations, remember useful information, work with
personal documents and provide personalized responses.

---

## 🚀 Features

### 🤖 AI Conversation

Pixotic uses Google Gemini to generate natural and conversational AI
responses.

It can communicate in:

- 🇬🇧 English
- 🇮🇳 Hindi
- 💬 Hinglish

---

### 🧠 Personal Memory

Pixotic includes a persistent memory system.

You can explicitly tell Pixotic to remember something:

```text
/remember My favorite cartoon is Tom and Jerry
```

View saved memories:

```text
/memory
```

Clear your memories:

```text
/forget
```

---

### 📚 RAG & Document Search

Pixotic can work with personal documents and retrieve relevant
information before generating an answer.

The RAG pipeline includes:

```text
Documents
    ↓
Text Extraction
    ↓
Text Chunking
    ↓
Embeddings
    ↓
Vector Database
    ↓
Relevant Context
    ↓
Gemini
    ↓
AI Response
```

This allows Pixotic to answer questions based on your own documents.

Example:

```text
What skills are mentioned in my CV?
```

```text
What projects are listed in my resume?
```

```text
What technologies are mentioned in my documents?
```

---

## 🐱🐭 Personalized Experience

Pixotic can remember personal preferences when the user explicitly
asks it to.

For example:

> My favorite cartoon is Tom and Jerry.

Pixotic can then use this information when it is relevant to the
conversation.

This is one of the ideas behind making Pixotic more personal than a
normal chatbot.

---

## 🎬 Media System

Pixotic is designed to go beyond text-only responses.

The project can be extended with personal media libraries such as:

```text
images/
gif/
videos/
```

This can allow Pixotic to respond with:

- 🖼️ Images
- 🎬 Short videos
- 😂 GIFs
- 🐱🐭 Favorite cartoon media

For example:

```text
Show me my Tom and Jerry GIF.
```

or:

```text
Show me a funny GIF.
```

---

## 📱 Telegram Integration

Pixotic runs through Telegram, allowing the assistant to be accessed
from a phone, desktop or any Telegram-supported device.

The basic flow is:

```text
User
  ↓
Telegram
  ↓
Pixotic
  ↓
Memory / RAG / AI
  ↓
Gemini
  ↓
Response
  ↓
Telegram
```

---

## 🏗️ Architecture

```text
                    ┌─────────────────┐
                    │     TELEGRAM    │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │     PIXOTIC     │
                    │  AI ASSISTANT   │
                    └────────┬────────┘
                             │
             ┌───────────────┼───────────────┐
             │               │               │
             ▼               ▼               ▼
      ┌────────────┐  ┌────────────┐  ┌────────────┐
      │  GEMINI AI │  │   MEMORY   │  │    RAG     │
      │             │  │   SQLite   │  │  ChromaDB  │
      └────────────┘  └────────────┘  └────────────┘
                             │               │
                             │               ▼
                             │        ┌────────────┐
                             │        │ Documents  │
                             │        │ PDF / TXT  │
                             │        └────────────┘
                             │
                             ▼
                      Personal Context
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| 🐍 Python | Core application |
| 📱 Telegram Bot API | User interface |
| 🤖 Google Gemini | AI generation |
| 🧠 SQLite | Persistent memory |
| 🔗 LangChain | RAG pipeline |
| 🔍 ChromaDB | Vector database |
| 🤗 Sentence Transformers | Text embeddings |
| 📄 PyPDF | PDF text extraction |

---

## 📁 Project Structure

```text
Pixotic-ai-bot/
│
├── pixotic.py
├── pixoticintro.mp4
├── README.md
├── requirements.txt
├── .env.example
├── .gitignore
│
├── memory/
│   ├── __init__.py
│   └── memory.py
│
├── cv/
│   └── your-documents.pdf
│
├── images/
│
├── gif/
│
└── data/
    └── pixotic_memory.db
```

> ⚠️ Personal documents and databases should not be committed to a
> public repository.

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/divanshusingh-ds/Pixotic-ai-bot.git
```

Enter the project directory:

```bash
cd Pixotic-ai-bot
```

---

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

---

### 3. Create your `.env` file

Create a file named:

```text
.env
```

Add:

```env
TELEGRAM_BOT_TOKEN=your_telegram_bot_token
GEMINI_API_KEY=your_gemini_api_key
```

**Never publish your real API keys or Telegram bot token.**

---

### 4. Run Pixotic

```bash
python pixotic.py
```

If everything is configured correctly, you should see:

```text
PIXOTIC FILE STARTED
🚀 Starting Pixotic AI Assistant...
🧠 Memory database ready.
🤖 Pixotic AI Assistant is running!
📱 Waiting for Telegram messages...
```

---

## 🧠 Memory Commands

| Command | Function |
|---|---|
| `/start` | Start Pixotic |
| `/remember` | Save information |
| `/memory` | View saved memories |
| `/forget` | Delete saved memories |

Example:

```text
/remember My favorite cartoon is Tom and Jerry
```

Then:

```text
/memory
```

---

## 📚 RAG Example

Place supported documents inside the project document folder.

For example:

```text
cv/
├── resume.pdf
├── notes.txt
└── course.pdf
```

Pixotic can then retrieve relevant information from those documents.

---

## 🔐 Security

Before pushing this project to GitHub, make sure sensitive files are
ignored.

Recommended `.gitignore`:

```gitignore
.env

__pycache__/
*.pyc

data/
*.db

agent_db/
chroma_db/

cv/
```

Do not upload:

```text
❌ .env
❌ Telegram Bot Token
❌ Gemini API Key
❌ Private CV
❌ Personal documents
❌ Private database
```

---

## 🗺️ Roadmap

### ✅ Completed

- [x] Telegram bot
- [x] Gemini AI integration
- [x] AI conversation
- [x] Persistent memory
- [x] SQLite memory database
- [x] PDF processing
- [x] Text chunking
- [x] Embeddings
- [x] RAG foundation
- [x] ChromaDB integration
- [x] Personalized responses

### 🚧 In Development

- [ ] Automatic memory extraction
- [ ] Image responses
- [ ] GIF responses
- [ ] Short video responses
- [ ] Favorite cartoon media
- [ ] Better RAG retrieval
- [ ] Conversation history
- [ ] Voice input
- [ ] Voice responses
- [ ] Web search
- [ ] Tool calling
- [ ] Image understanding

### 🔮 Future

- [ ] Pixotic web interface
- [ ] Advanced AI agent
- [ ] Multi-modal conversations
- [ ] Smart media recommendations
- [ ] Personalized AI environment
- [ ] Cloud deployment

---

## 🌟 Vision

Pixotic is being developed as more than a simple Telegram chatbot.

The long-term vision is to build a personal AI assistant that can:

```text
Understand
    ↓
Remember
    ↓
Search
    ↓
Reason
    ↓
Interact
    ↓
Personalize
```

The goal is to make Pixotic feel less like a traditional chatbot and
more like a personal AI assistant.

---

## 💡 Project Philosophy

> **Your AI. Your Memory. Your World.**

Pixotic is an ongoing project focused on exploring how AI can become
more personal, useful and interactive.

---

## 👨‍💻 Author

**Divanshu Singh**

Building **Pixotic AI Assistant** with Python, Gemini and Telegram.

---

<p align="center">
  🤖 <strong>PIXOTIC AI ASSISTANT</strong>
</p>

<p align="center">
  <i>Building a personal AI assistant, one feature at a time.</i>
</p>
