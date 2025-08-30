# Resume Score

## Introduction

Resume Score is an intelligent resume evaluation tool designed to simplify and accelerate the hiring pipeline. By combining Natural Language Processing (NLP) with modern machine learning models, the system automatically parses resumes, interprets job descriptions, and delivers compatibility scores that help recruiters make data-driven hiring decisions.

## Core Capabilities

- Smart Resume Parsing:
  - Extracts structured data (skills, education, experience) from unstructured CVs using NLP.
- Context-Aware Matching:
  - Measures alignment between resumes and job requirements through semantic similarity models.
- Layered Processing Pipeline:
  - Preprocessing and text normalization
  - Resume section identification
  - Named entity recognition (NER)
  - Scoring using semantic similarity + vector space models
- Interactive Web Interface:
  - Upload resumes and job descriptions through a React-based frontend.
- Scalable API Service:
  - Powered by FastAPI and designed for fast, asynchronous processing.

## Tech Stack

- Frontend → React, Tailwind
- Backend → FastAPI, Uvicorn
- NLP / ML → spaCy, Sentence Transformers, NER
- Similarity Models → Cosine similarity, TF-IDF

## Achievements

- Handles a curated database of ~2,000 professional skills
- Blends rule-based and ML-driven entity recognition
- Produces ranked candidate lists with compatibility scores
- Correlates ~0.70 with human evaluations


## Project Components

### Frontend Components

1. **Landing Page** (`pages/LandingPage.jsx`)
   - Project introduction
   - Feature showcase
   - Technology stack overview

2. **Screening Page** (`pages/ScreeningPage.jsx`)
   - Resume upload interface
   - Job description input
   - Real-time analysis display

3. **Ranking Page** (`pages/RankPage.jsx`)
   - Batch processing interface
   - Comparative analysis
   - Ranking visualization

### Backend Components

1. **Main Application** (`app.py`)
   - API endpoint definitions
   - Request handling
   - File management

2. **Information Extraction** (`extractInformation.py`)
   - Resume parsing logic
   - Text preprocessing
   - Entity extraction

3. **Scoring Modules** (`model/` directory)
   - `degreeScore.py`: Education evaluation
   - `experienceScore.py`: Work experience analysis
   - `skillScore.py`: Technical skills matching
   - `softSkillScore.py`: Soft skills evaluation
   - `majorScore.py`: Field of study analysis

## Usage Tips

1. **Resume Format**
   - Supported formats: PDF

2. **Job Description**
   - Be specific with requirements
   - Include both technical and soft skills
   - Specify education and experience requirements

3. **Batch Processing**
   - Upload multiple resumes for comparison
   - Use consistent job descriptions for better results

## Troubleshooting

Common issues and solutions:

1. **Backend Connection Issues**
   - Verify the FastAPI server is running
   - Check port availability (8000)
   - Confirm CORS settings

2. **File Upload Problems**
   - Check file format (PDF only)

3. **Processing Errors**
   - Check Python environment
   - Verify all dependencies are installed

## Setup Guide

### Requirements

- Frontend: Node.js + Yarn
- Backend: Python 3.7+, FastAPI, Uvicorn

## Installation Steps
1. Clone the Repository
```
git clone https://github.com/sewakshekokar/Resume-Score
cd "Resume Score"
```

2. Frontend Setup
```
cd frontend
yarn install
yarn dev
```

3. Backend Setup
```
cd server
python3 -m venv .venv
source .venv/bin/activate   # Linux / macOS  
.venv\Scripts\activate    # Windows  

pip install -r requirements.txt
uvicorn app:app --reload
```

## How to use
1. Start the frontend (http://localhost:3000) and the backend.
2. Upload one or multiple resumes.
3. Paste job description.

## Known Constraints

- Limited performance on highly complex or unusual resume layouts.
- Mostly optimized for English-language resumes.

## Team Members
- Rohan
- Sevak Shekokar
- Krishna Kumar Bais
