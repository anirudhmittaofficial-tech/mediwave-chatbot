# 🤖 AI Medicine Information Chatbot

> **Internship Project — Mediwave Life Sciences Pvt Ltd**  
> 4-Week Internship Program | June 2026 | Aurora Deemed to be University

---

## 📋 Project Overview

The **AI Medicine Information Chatbot** is a full-stack web application built for **Mediwave Life Sciences Pvt Ltd** — a pharmaceutical company operating in drug distribution, pharmacy ordering, inventory management, and medical representative operations.

The chatbot allows pharmacies, doctors, and patients to ask product-related questions and receive accurate, real-time responses sourced directly from Mediwave's product catalogue — with **mandatory medical disclaimers** on every response.

---

## ❗ Problem Statement

Currently, Mediwave's staff manually handles repeated product information queries through calls, WhatsApp messages, and spreadsheets. This results in:

- Slow query resolution and delayed responses
- Risk of medical misinformation through inconsistent answers
- Missed revenue opportunities due to delayed follow-ups
- No audit trail or ownership tracking for customer interactions

---

## ✅ Solution

An AI-powered chatbot that:

- Answers product-related questions instantly from the company knowledge base
- Detects user intent using OpenAI / Gemini API
- Injects safe medical disclaimers automatically on every response
- Routes complex or sensitive queries to a human agent (handover workflow)
- Provides an admin dashboard for tracking conversations, priorities, and history

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | HTML, CSS, JavaScript / React |
| **Backend** | Python Flask / Node.js Express |
| **AI Layer** | OpenAI API / Google Gemini API |
| **Database** | MySQL / PostgreSQL / Firebase |
| **Messaging & Reports** | WhatsApp Business API / Email API / PDF Export |

---

## 🗂️ Project Structure

```
mediwave-chatbot/
│
├── frontend/
│   ├── index.html              # Main chat UI entry point
│   ├── css/
│   │   └── style.css           # Styling for chat, FAQ, dashboard
│   ├── js/
│   │   └── app.js              # Frontend logic, API calls
│   └── components/
│       ├── ChatWindow.jsx       # Chat interface component
│       ├── FAQScreen.jsx        # FAQ listing screen
│       ├── EnquiryForm.jsx      # Enquiry capture form
│       └── HandoverDashboard.jsx# Admin handover view
│
├── backend/
│   ├── app.py                  # Flask app entry point (or server.js for Express)
│   ├── routes/
│   │   ├── chat.py             # Conversation endpoint
│   │   ├── products.py         # Product data endpoints
│   │   └── handover.py         # Agent handover logic
│   ├── services/
│   │   ├── ai_service.py       # OpenAI / Gemini API integration
│   │   ├── knowledge_base.py   # FAQ retrieval & product lookup
│   │   └── disclaimer.py       # Medical disclaimer injection
│   └── models/
│       ├── product.py          # Product schema
│       ├── conversation.py     # Conversation history schema
│       └── pharmacy.py         # Pharmacy/user schema
│
├── database/
│   └── schema.sql              # MySQL/PostgreSQL database schema
│
├── tests/
│   ├── test_chat_api.py        # API endpoint tests
│   ├── test_ai_responses.py    # AI response quality tests
│   └── test_handover.py        # Handover workflow tests
│
├── docs/
│   ├── Week1_Presentation.pptx
│   └── Final_Report.pdf
│
├── .env.example                # Environment variable template
├── requirements.txt            # Python dependencies
├── package.json                # Node.js dependencies (if applicable)
└── README.md
```

---

## ⚙️ Setup & Installation

### Prerequisites

- Python 3.9+ or Node.js 18+
- MySQL / PostgreSQL / Firebase account
- OpenAI API key or Google Gemini API key

### 1. Clone the Repository

```bash
git clone https://github.com/[your-username]/mediwave-chatbot.git
cd mediwave-chatbot
```

### 2. Set Up Environment Variables

```bash
cp .env.example .env
```

Edit `.env` and fill in your keys:

```env
OPENAI_API_KEY=your_openai_api_key_here
GEMINI_API_KEY=your_gemini_api_key_here
DB_HOST=localhost
DB_NAME=mediwave_db
DB_USER=root
DB_PASSWORD=your_password
```

### 3. Install Backend Dependencies

```bash
# Python (Flask)
pip install -r requirements.txt

# OR Node.js (Express)
npm install
```

### 4. Set Up the Database

```bash
mysql -u root -p < database/schema.sql
```

### 5. Run the Application

```bash
# Flask
python backend/app.py

# OR Express
node backend/server.js
```

### 6. Open the Frontend

Open `frontend/index.html` in your browser, or if using React:

```bash
cd frontend
npm install
npm start
```

---

## 🔄 How It Works

```
User Query (Chat UI / FAQ Screen)
        ↓
Backend API — validates input, saves with timestamp + source
        ↓
AI Layer — detects intent, retrieves from knowledge base
        ↓
Response generated with mandatory medical disclaimer
        ↓
Complex queries → Handover Workflow → Admin/MR notified
        ↓
Admin Dashboard — full history, status, priorities
```

---

## 🎯 Project Objectives

1. **Design** a conversational chat UI with FAQ screens and handover dashboard
2. **Develop** backend REST APIs for conversation flow and knowledge base management
3. **Integrate** OpenAI / Gemini API for intent detection and safe medical responses
4. **Implement** a database to store products, medicines, orders, and conversation history
5. **Deploy & Document** the working prototype with test report, GitHub, and demo video

---

## 📅 Development Timeline

| Week | Dates | Focus |
|------|-------|-------|
| Week 1 | Jun 1–6 | Research, problem analysis, UI wireframes, presentation |
| Week 2 | Jun 9–13 | Frontend + Backend core development |
| Week 3 | Jun 16–20 | AI integration, intent detection, admin dashboard |
| Week 4 | Jun 23–27 | Testing, deployment, documentation, demo video |

---

## 🧪 Testing

```bash
# Run all tests
pytest tests/

# Run specific test file
pytest tests/test_chat_api.py -v
```

---

## 👤 Team & Roles

| Role | Responsibility |
|------|---------------|
| **Frontend Developer** | Chat UI, FAQ screens, enquiry form, conversation history, handover dashboard |
| **Backend Developer** | Conversation APIs, knowledge base, prompt templates, fallback & handover logic |
| **Testing & Deployment** | Manual testing, API testing, GitHub management, deployment validation |

> *Note: All three roles executed by a single developer for this internship build.*

---

## 📌 Key Features

- 💬 **Conversational Chat Interface** — clean, real-time chat UI
- 🔍 **Product Knowledge Base** — queries answered from Mediwave's catalogue
- 🛡️ **Medical Disclaimer Injection** — auto-appended to every AI response
- 🔁 **Agent Handover Workflow** — complex queries escalated to human agents
- 📊 **Admin Dashboard** — full conversation history, ownership, and priority tracking
- 📩 **Automated Notifications** — WhatsApp / email alerts for follow-ups

---

## ⚠️ Medical Disclaimer

> This chatbot is intended to provide **general product information only** and does not constitute medical advice. Always consult a qualified healthcare professional before making any medical decisions. Mediwave Life Sciences Pvt Ltd is not responsible for actions taken based on chatbot responses.

---

## 📄 License

This project was built as part of the **4-Week Internship Program** at Mediwave Life Sciences Pvt Ltd in collaboration with Aurora Deemed to be University. Not licensed for commercial use without permission.

---

## 🙏 Acknowledgements

- **Mediwave Life Sciences Pvt Ltd** — for providing the real-world business context
- **Aurora Deemed to be University** — for the internship program framework
- OpenAI / Google Gemini — for the AI API powering the chatbot

---

*Built with ❤️ by [Your Name] | Aurora Deemed to be University | June 2026*
