# AI Question Generator

This project is an AI-powered quiz platform that dynamically generates tailored multiple-choice challenges using OpenAI's API. Built with a fast, modern FastAPI backend and a responsive React/Vite frontend, the application includes robust user authentication via Clerk, tracking system mechanics for daily challenge quotas, difficulty scaling (Easy, Medium, Hard), and a detailed history log to monitor user progress.

# Features

- Leverages the OpenAI API to construct context-aware, high-quality multiple-choice questions on demand for any topic.
- Tailors the challenge complexity dynamically across **Easy**, **Medium**, and **Hard** presets to match user proficiency.
- Utilizes **Clerk** for robust, seamless user sign-ins, session management, and protected frontend/backend routing.
- Tracks and logs complete user performance metrics, allowing users to review past quizzes and monitor progress over time.
- Enforces structured pacing constraints by calculating and tracking daily user challenge limits.
- Backed by **SQLite** and managed via **SQLAlchemy ORM** to ensure reliable data persistence for quotas, history logs, and user states.
- Built on a modern **React + Vite** architecture to provide instantaneous view updates, seamless state handling, and zero-latency page transitions.

# Tech Stack

- **Frontend:** React, Vite, Clerk
- **Backend:** FastAPI, Uvicorn
- **AI/LLM:** OpenAI API
- **Auth:** Clerk
- **Database/State:** SQLite managed via SQLAlchemy ORM

# Prerequisites
- **Python 3.9+**
- **pip**
- **Node.js (v18.0.0+)**
- **OpenAI Account:** An active API key to generate the multiple-choice questions.
- **Clerk Account:** A Clerk application setup to handle user authentication

# Getting Started
Clone the repository:

```bash
git clone [https://github.com/edbucio24/ai-question-generator.git](https://github.com/edbucio24/ai-question-generator.git)
cd ai-question-generator
```
Setup Backend:
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload
```

Setup Frontend:
```bash
cd frontend
npm install
npm run dev
```

#Environment Setup:
Create a .env file in your backend directory:
```bash
OPENAI_API_KEY=your_openai_api_key_here
CLERK_SECRET_KEY=your_clerk_secret_key_here
JWT_SECRET_KEY=your_generated_jwt_secret_key_here
DATABASE_URL=sqlite:///./quiz_app.db
```

Create a .env.local file in your frontend directory:
```bash
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key_here
VITE_API_BASE_URL=http://localhost:8000
```

# License
This project is released under the MIT License.
