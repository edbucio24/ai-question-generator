# AI Question Generator
[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GitHub Issues](https://img.shields.io/github/issues/username/repo-name.svg)](https://github.com/username/repo-name/issues)
[![Haskell](https://img.shields.io/badge/Language-Haskell-purple.svg)](https://www.haskell.org/)

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

### Prerequisites
- **Python 3.9+**
- **pip**
- **Node.js (v18.0.0+)**
- **OpenAI Account:** An active API key to generate the multiple-choice questions.
- **Clerk Account:** A Clerk application setup to handle user authentication
