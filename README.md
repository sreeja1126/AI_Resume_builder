# AI Resume Portfolio Builder

A full-stack web application that uses AI to help users generate professional resumes, portfolios, and cover letters. Users fill in their personal information, skills, and experience, and the app uses OpenAI's GPT models to generate polished, ATS-friendly content — with a live preview and export options.

## Features

- **Resume builder** — input personal details, education, skills, and experience; the app generates formatted, professional resume content
- **Portfolio section** — structure and present projects alongside the resume
- **Cover letter generation** — AI-generated cover letter content based on the user's profile
- **Live preview** — see the formatted resume update as you edit
- **Export options** — download as PDF or Word, or print directly

## How it works

1. User enters their details through the React frontend (Home → Resume Builder → Portfolio → Cover Letter flow)
2. The frontend sends this data to a FastAPI backend
3. The backend calls the OpenAI API (GPT-3.5/GPT-4) to generate optimized, professional resume content — improving phrasing, keyword usage, and formatting for ATS compatibility
4. The generated content is returned and rendered in a live preview, ready to download or print

## Tech stack

**Frontend:** React, HTML, CSS, JavaScript
**Backend:** Python, FastAPI
**AI/ML:** OpenAI GPT-3.5 / GPT-4 API
**Tools:** REST API, JSON, python-dotenv, Git/GitHub

## Example output

Given basic input (name, contact info, a short professional summary, education, skills, and a one-line description of an internship), the app generates a structured resume preview including an expanded, professionally worded experience section — for example, turning a brief internship description into a detailed bullet-pointed summary covering responsibilities, technologies used, and outcomes, formatted for direct export.

## Setup

**Backend:**
```bash
git clone https://github.com/sreeja1126/AI_Resume_builder.git
cd AI_Resume_builder

# create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate      # on Windows: venv\Scripts\activate

pip install -r requirements.txt

# set your OpenAI API key
export OPENAI_API_KEY=your_api_key_here   # on Windows: set OPENAI_API_KEY=your_api_key_here

uvicorn main:app --reload
```

**Frontend:**
```bash
cd frontend
npm install
npm start
```

The frontend will run at `http://localhost:3000` and connect to the backend API.

## Current limitations

- Download (PDF/Word) and print functions are still being finalized
- Portfolio/projects section is not yet fully wired to the generation pipeline
- No persistent storage yet — data doesn't currently save between sessions

## Why I built this

Most resume builders use rigid templates that don't adapt to what makes an individual's background stand out. I wanted to build something that actually uses generative AI to improve and tailor content — not just fill in a template — while learning how to connect a React frontend to a Python AI backend in a real full-stack flow.
