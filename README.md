## Asha AI Chatbot
Asha AI Chatbot is an AI-powered career assistant designed to support users in their professional journey by providing job opportunities, career-related events, mentorship guidance, and intelligent career advice through natural language conversations.
The system combines a FastAPI-based backend with a lightweight web frontend and integrates Large Language Models along with real-world APIs to deliver reliable, context-aware, and user-friendly interactions.
_______________________________________

## Project Structure Overview

AshaAiChatbot
│
├── backend
│   │
│   ├── main.py               (FastAPI application entry point)
│   ├── chat_memory.py        (Multi-turn conversation memory handling)
│   ├── database.py           (Database connection and ORM logic)
│   ├── crypto_utils.py       (Encryption and security utilities)
│   ├── events.py             (Career events integration – Eventbrite)
│   ├── intent_classifier.py  (User intent detection and routing)
│   ├── job_listings.py       (Job search services – Jooble & Remotive)
│   ├── location.py           (User location detection utilities)
│   ├── mistral_client.py     (LLM integration via OpenRouter)
│   ├── chatbot.db            (SQLite database)
│   └── .env.template         (Environment variable template)
│
├── frontend
│   │
│   ├── index.html            (User interface)
│   ├── style.css             (Styling and layout)
│   ├── script.js             (Client-side logic and API calls)
│   └── logo.png              (Application branding)
│
└── README.md                 (Project documentation)

────────────────────────────────────

## Backend Setup Instructions

Navigate to the backend directory using a terminal. Create a virtual environment and activate it according to your operating system. Install the required dependencies including FastAPI, Uvicorn, python-dotenv, SQLAlchemy, cryptography, and requests.

Create a `.env` file by copying the provided `.env.template` and configure the necessary API keys such as OpenRouter, Jooble, Eventbrite, and IPInfo. Once configured, start the FastAPI server using Uvicorn. The backend service will be available at:

http://127.0.0.1:8000

────────────────────────────────────

## Frontend Setup Instructions

Navigate to the frontend directory and open `index.html` directly in a web browser. Ensure that the backend server is running before interacting with the chatbot to enable proper communication between the frontend and backend.

────────────────────────────────────

## Chatbot Capabilities

The chatbot supports multi-turn conversation memory, detects offensive or biased inputs, provides job listings from Jooble and Remotive, fetches career events using Eventbrite, and offers AI-driven fallback responses using the Mistral model via OpenRouter. Chat history is preserved across page refreshes, sessions are managed using cookies, and users can clear conversation history when required.

────────────────────────────────────

## Important Notes

If the chatbot displays a connection error, verify that the backend server is active and running. Environment variables and API keys must remain confidential and should never be committed to version control. External APIs may occasionally be rate-limited, and the chatbot is designed to handle such situations gracefully.

────────────────────────────────────

## Future Enhancements

Planned improvements include user authentication (login and signup), voice-to-text interaction, deployment to cloud platforms such as Render or Railway, enhanced database design for long-term career tracking, and further user interface refinements.

────────────────────────────────────

## Contributors
Akshaya N E  
Mirunalini A  
