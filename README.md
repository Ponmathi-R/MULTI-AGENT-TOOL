# 🤖 Multi-Agent AI Assistant using n8n

## 📌 Overview

The **Multi-Agent AI Assistant** is an intelligent automation workflow built using **n8n**, **OpenAI GPT-4.1 Mini**, and **Telegram**. It acts as a personal AI assistant capable of understanding natural language requests and automatically selecting the appropriate tool to complete the task.

The AI Agent integrates with multiple Google services and external APIs, allowing users to perform tasks such as sending emails, updating Google Sheets, editing Google Docs, scheduling Google Calendar events, and searching the internet—all from a simple Telegram chat.

---

# 🚀 Features

* 📱 Telegram Bot Interface
* 🧠 OpenAI GPT-4.1 Mini AI Agent
* 💬 Conversation Memory
* 📧 Gmail Integration
* 📅 Google Calendar Integration
* 📊 Google Sheets Integration
* 📄 Google Docs Integration
* 🌐 Internet Search using SerpAPI
* 🤖 Automatic Tool Selection
* 💡 Natural Language Understanding
* 🕒 IST Time Awareness
* 🔄 Multi-Agent Tool Calling Architecture

---

# 🛠 Tech Stack

* n8n
* OpenAI GPT-4.1 Mini
* Telegram Bot API
* Gmail API
* Google Calendar API
* Google Sheets API
* Google Docs API
* SerpAPI
* JSON Workflow

---

# 🏗 Workflow Architecture

```text
                  User
                    │
                    ▼
           Telegram Bot Trigger
                    │
                    ▼
          OpenAI GPT-4.1 Mini Agent
                    │
         ┌──────────┼──────────┐
         │          │          │
         ▼          ▼          ▼
     Gmail      Calendar     SerpAPI
         │          │
         ▼          ▼
 Google Docs   Google Sheets
         │
         ▼
     AI Response
         │
         ▼
 Telegram Reply
```

---

# 📋 Workflow Components

## 1. Telegram Trigger

* Starts the workflow when a new Telegram message is received.
* Captures the user's request.

---

## 2. AI Agent

The AI Agent acts as the central controller.

Responsibilities:

* Understands user intent
* Chooses the appropriate tool
* Maintains conversation flow
* Executes tool calls automatically
* Generates natural language responses

System prompt capabilities include:

* Send Email
* Search the Internet
* Update Google Sheets
* Edit Google Docs
* Schedule Calendar Events
* Follow IST timezone

---

## 3. OpenAI Chat Model

**Model Used**

* GPT-4.1 Mini

Responsible for:

* Intent recognition
* Reasoning
* Tool selection
* Response generation

---

## 4. Memory

Uses **Buffer Window Memory**.

Stores the previous **3 conversations** to provide contextual responses.

---

## 5. Gmail Tool

Capabilities:

* Compose emails
* Send emails
* Generate professional email content

Example:

> "Send an email to John saying tomorrow's meeting is postponed."

---

## 6. Google Calendar Tool

Capabilities:

* Create calendar events
* Schedule meetings
* Block time
* Follow IST timezone

Example:

> "Schedule a meeting tomorrow at 3 PM."

---

## 7. Google Sheets Tool

Capabilities:

* Append new rows
* Store student details
* Update spreadsheet records

Example:

> "Add Rahul to the student sheet."

---

## 8. Google Docs Tool

Capabilities:

* Insert text
* Update documents
* Generate reports

Example:

> "Create today's meeting notes."

---

## 9. SerpAPI

Provides real-time internet search.

Example:

> "Search for the latest AI news."

---

## 10. Telegram Output

Returns the AI-generated response directly to the Telegram chat.

---

# 📂 Workflow Sequence

```text
User Message
      │
      ▼
Telegram Trigger
      │
      ▼
AI Agent
      │
      ▼
OpenAI GPT-4.1 Mini
      │
      ▼
Select Required Tool
      │
      ├── Gmail
      ├── Google Calendar
      ├── Google Sheets
      ├── Google Docs
      └── SerpAPI
      │
      ▼
Tool Executes Task
      │
      ▼
Telegram Reply
```

---

# 📦 Prerequisites

Before running the workflow, ensure you have:

* n8n (Local or Cloud)
* Telegram Bot Token
* OpenAI API Key
* Gmail OAuth Credentials
* Google Calendar OAuth Credentials
* Google Sheets OAuth Credentials
* Google Docs OAuth Credentials
* SerpAPI Key

---

# 🔑 Required Credentials

### Telegram

* Telegram Bot Token

### OpenAI

* API Key
* Model: GPT-4.1 Mini

### Gmail

* OAuth2 Credential

### Google Calendar

* OAuth2 Credential

### Google Sheets

* OAuth2 Credential

### Google Docs

* OAuth2 Credential

### SerpAPI

* API Key

---

# 💬 Example Commands

### Email

> Send an email to [john@example.com](mailto:john@example.com) saying the meeting is postponed.

### Calendar

> Schedule a meeting tomorrow at 4 PM.

### Google Sheets

> Add Rahul, GenAI Course, Enrolled, [rahul@gmail.com](mailto:rahul@gmail.com).

### Google Docs

> Create today's project meeting notes.

### Internet Search

> Search for the latest OpenAI news.

---

# 📁 Project Structure

```text
Multi-Agent-AI-Assistant/
│
├── README.md
├── multi_agent_workflow.json
└── screenshots/
    ├── workflow.png
    ├── telegram_chat.png
    ├── gmail.png
    ├── sheets.png
    ├── calendar.png
    └── docs.png
```

---

# 🔮 Future Enhancements

* Voice commands
* WhatsApp integration
* Slack integration
* Microsoft Teams integration
* PDF generation
* File upload analysis
* Image generation
* OCR support
* CRM integration
* Database connectivity
* Multi-language support
* RAG with document retrieval
* Memory using vector databases

---

# 📊 Workflow Summary

| Component           | Purpose                              |
| ------------------- | ------------------------------------ |
| Telegram Trigger    | Receives user messages               |
| AI Agent            | Understands intent and selects tools |
| OpenAI GPT-4.1 Mini | Natural language reasoning           |
| Memory              | Maintains conversation context       |
| Gmail               | Sends emails                         |
| Google Calendar     | Creates calendar events              |
| Google Sheets       | Updates spreadsheets                 |
| Google Docs         | Creates or edits documents           |
| SerpAPI             | Performs internet searches           |
| Telegram Output     | Returns the final response           |

---

# 👨‍💻 Author

**Ponmathi Radhakrishnan**

**Built with:** n8n • OpenAI GPT-4.1 Mini • Telegram • Gmail • Google Workspace • SerpAPI
