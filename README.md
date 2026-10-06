# TrendVista – Global News Trend Analyzer Using AI

> AI-powered platform for collecting, analyzing, and visualizing global news trends using Natural Language Processing (NLP), topic modeling, sentiment analysis, Named Entity Recognition (NER), trend detection, and interactive dashboards.

## Table of Contents

- [Abstract](#abstract)
- [Introduction](#introduction)
- [Objectives](#objectives)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [System Architecture](#system-architecture)
- [Modules](#modules)
- [NLP and AI Pipeline](#nlp-and-ai-pipeline)
- [Database](#database)
- [Frontend](#frontend)
- [Backend and APIs](#backend-and-apis)
- [Authentication](#authentication)
- [Dashboards and User Features](#dashboards-and-user-features)
- [Implementation](#implementation)
- [Testing](#testing)
- [Project Setup](#project-setup)
- [Project Structure](#project-structure)
- [Future Enhancements](#future-enhancements)
- [Conclusion](#conclusion)
- [Documentation](#documentation)

---

## Abstract

TrendVista is an AI-powered platform that collects, analyzes, and visualizes global news trends in real time. The system is designed to provide a centralized and interactive platform that not only displays categorized news but also extracts meaningful patterns and insights from news content.

The platform applies sentiment analysis, Named Entity Recognition (NER), keyword extraction, topic modeling, and trend identification to transform unstructured news text into structured and actionable information.

TrendVista includes user authentication, personalized news filtering, trending news, interactive dashboards, voice-based search using the Speech Recognition API, raw text analysis, article comparison, bookmarks, geo-tagging, and an administrator dashboard.

The frontend uses React.js and Tailwind CSS. The backend is implemented using Python-based API services, primarily FastAPI. Supabase/PostgreSQL is used for data storage. NLP functionality is implemented using libraries and models including spaCy, NLTK, Transformers, KeyBERT, BERTopic, LDA, scikit-learn, Gensim, and Sentence Transformers.

---

## Introduction

### Overview

People receive news from many websites, applications, and social media platforms. The large amount of information available online makes it difficult to identify reliable, relevant, and easy-to-understand news.

TrendVista addresses this problem by providing an AI-powered news analyzer that processes and interprets global news articles using machine learning and NLP.

The platform provides:

- Sentiment reports
- Trending keywords
- Topic clusters
- Named entities
- Time-based trend graphs
- Category-wise analysis
- Interactive dashboards
- Search and filtering
- Article comparison
- Bookmarking
- Voice search
- Geo-tagging

TrendVista can support students, researchers, analysts, journalists, and policymakers.

### Background and Motivation

The project is motivated by:

- Increasing misinformation and information overload online
- Difficulty identifying trending or critical issues
- The need to summarize large volumes of text
- Growing demand for AI-based insights in journalism, policy, and social sciences
- The need for intelligent dashboards in modern applications

### Core Functionality

1. User authentication
2. News/article fetching
3. NLP analysis
4. Sentiment analysis
5. Named Entity Recognition
6. Keyword extraction
7. Topic modeling
8. Trend detection
9. Interactive dashboards
10. Admin management

---

## Objectives

The main objectives of TrendVista are:

1. Develop a centralized news platform displaying latest and trending articles across categories such as politics, technology, business, entertainment, and sports.
2. Implement secure user registration, login, logout, and profile management.
3. Build a responsive React.js frontend.
4. Develop a reliable Python/FastAPI backend for API endpoints and database operations.
5. Integrate RESTful APIs for frontend-backend communication.
6. Provide search and filtering based on keywords and categories.
7. Display recent and trending news dynamically.
8. Provide user profile and preference management.
9. Apply modern full-stack development practices.
10. Deliver a deployable application following industry-oriented UI/UX, code structure, and performance practices.

---

## Key Features

### User Features

- User registration and login
- JWT-based authentication
- Profile management
- Personalized preferences
- News category filtering
- Trending news
- Search
- Voice search
- Raw text analysis
- Sentiment analysis
- Named Entity Recognition
- Keyword extraction
- Topic exploration
- Article comparison
- Bookmark/save articles
- Geo-tagging and location-based news
- Interactive trend dashboards

### Admin Features

- Protected admin dashboard
- View total users
- View admin users
- View regular users
- Delete users
- Manage user accounts
- Monitor system health
- View advanced analytics
- View trending topics
- View sentiment distribution
- Monitor platform activity

---

## Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React.js |
| Styling | Tailwind CSS |
| Backend | FastAPI / Python |
| API | RESTful APIs |
| Database | Supabase / PostgreSQL |
| ORM | SQLAlchemy |
| Authentication | JWT |
| Password Security | Passlib / bcrypt |
| NLP | spaCy, NLTK, Transformers |
| Sentiment | NLTK, Transformer-based models |
| NER | spaCy / Transformer-based NER |
| Keyword Extraction | KeyBERT |
| Topic Modeling | BERTopic, LDA/NMF |
| ML / Processing | scikit-learn, NumPy, Pandas |
| Embeddings | Sentence Transformers |
| Topic Processing | Gensim |
| Visualization | Recharts / chart libraries |
| Maps | Leaflet.js |
| Version Control | Git and GitHub |
| IDE | Visual Studio Code |
| Design | Figma / Canva |
| Development Server | Uvicorn |
| Deployment | Docker / Render |
| Browser Testing | Chrome / Edge |

---

## System Architecture

TrendVista follows a layered architecture.

### 1. Frontend Layer

The React.js frontend:

- Provides the user interface
- Handles user interaction
- Displays news and analysis results
- Sends requests to backend APIs
- Displays dashboards and visualizations
- Provides authentication and profile pages

### 2. Backend Layer

The backend:

- Handles API endpoints
- Performs business logic
- Manages authentication
- Communicates with the database
- Processes news data
- Runs NLP analysis
- Generates trend insights

### 3. Data Layer

Supabase/PostgreSQL stores structured application data such as:

- Users
- User profiles
- Articles
- Preferences
- Related project data

### External Data Sources

The documentation identifies external news sources/APIs including:

- NewsAPI
- GNews
- Reddit API

---

## Modules

### Module 1 – User Authentication and Profile Management

Purpose: provide secure registration, login, logout, protected sessions, and user preferences.

#### Authentication

- User registration
- Login
- Logout
- Password hashing
- JWT token generation
- JWT token verification
- Protected routes
- Unauthorized-access protection

#### Profile Management

Users can manage:

- Name
- Language
- Interests
- News preferences
- Other profile information

---

### Module 2 – Core NLP Analysis

This is the main analytical engine of TrendVista.

#### Text Processing

The system preprocesses raw text using operations such as:

- Tokenization
- Stop-word removal
- Stemming
- Lemmatization
- Text normalization

Example:

```text
Input:
"India's economy is growing faster in 2025?"

Processed representation:
"india economy grow fast"
```

#### Sentiment Analysis

The system classifies news/text into:

- Positive
- Negative
- Neutral

The documentation describes the use of NLTK-based sentiment processing and transformer-based sentiment models.

The API can return sentiment labels, confidence scores, and related scores.

#### Named Entity Recognition

NER identifies entities such as:

- PERSON
- ORGANIZATION
- LOCATION
- Products
- Dates

The system uses spaCy and transformer-based NER approaches.

Example:

```text
PERSON       → person names
ORG          → organizations
LOC          → locations
```

#### Keyword Extraction

KeyBERT is used to identify important keywords and short phrases from articles.

The extracted keywords can be used for:

- Topic discovery
- Trend analysis
- Search
- Article analysis
- Visualization

---

### Module 3 – Topic Modeling and Trend Identification

The purpose of this module is to analyze time-based topic and sentiment patterns and identify emerging trends.

#### Topic Modeling

The project documentation describes:

- BERTopic as a primary approach
- LDA/NMF as fallback approaches
- NLTK/spaCy preprocessing
- Keyword extraction
- Topic labeling

#### Time-Series Trend Analysis

Pandas and NumPy are used to analyze topic and sentiment frequency over time.

The system can analyze:

- Daily trends
- Weekly trends
- Monthly trends
- Topic frequency
- Sentiment variation
- Spikes in mentions
- Declining trends

#### Sentiment per Topic / Entity

Sentiment results can be associated with topics and entities to understand how sentiment changes around particular subjects.

Example:

```text
Technology → Positive sentiment
Politics   → Negative sentiment
```

#### Trend Dashboard

The dashboard can display:

- Top trending topics
- Top keywords
- Sentiment distribution
- Sentiment trends over time
- Interactive charts
- Time-range filters

---

### Module 4 – Advanced Insights, Admin and Deployment

This module provides:

- Advanced trend analysis
- Correlation of sentiment, entities, and trends
- Admin management
- System monitoring
- Advanced analytics
- Deployment support

---

## NLP and AI Pipeline

The general processing flow is:

```text
News APIs / Feeds
        ↓
Data Ingestion
        ↓
Text Cleaning & Preprocessing
        ↓
Sentiment Analysis
        ↓
Named Entity Recognition
        ↓
Keyword Extraction
        ↓
Topic Modeling
        ↓
Trend Detection
        ↓
Database / Insights
        ↓
React Dashboards
```

### NLP Technologies

| Technology | Purpose |
|---|---|
| spaCy | NER and NLP processing |
| NLTK | Text preprocessing and sentiment |
| Transformers | Transformer-based NLP and sentiment |
| KeyBERT | Keyword extraction |
| BERTopic | Topic modeling |
| LDA/NMF | Topic modeling fallback |
| scikit-learn | TF-IDF and ML preprocessing |
| Gensim | Topic modeling |
| Sentence Transformers | Text embeddings and similarity |
| PyTorch | Deep-learning model execution |
| Pandas | Data processing |
| NumPy | Numerical analysis |

---

## Database

The project uses Supabase with PostgreSQL.

### Users

| Column | Type | Description |
|---|---|---|
| id | Integer | Unique user identifier |
| email | String | Registered email |
| hashed_password | String | Secured password |

### Profile Preferences

| Column | Type | Description |
|---|---|---|
| id | Integer | Profile ID |
| user_id | Integer | Reference to user |
| preferred_language | String | User language |
| interests | String/JSON | User interests/topics |

### Articles

| Column | Type | Description |
|---|---|---|
| id | Integer | Article ID |
| title | String | News headline |
| source | String | Publisher/source |
| publishedAt | DateTime | Publication date |
| url | String | Article URL |
| description | Text | Article summary/description |
| image | String | Thumbnail URL |

The documentation also shows additional database structures for user profiles and password reset tokens.

---

## Frontend

The frontend is built with React.js and Tailwind CSS.

### Main Screens

- Register
- Login
- Dashboard/Home
- Trending News
- Trend Explorer
- Text Analysis
- Compare Articles
- Bookmarks
- Profile Management
- Settings
- Geo Dashboard
- Admin Dashboard

### Frontend Libraries

- React
- Axios
- React Router DOM
- Lucide React
- Framer Motion
- Recharts
- Leaflet

---

## Backend and APIs

The backend provides RESTful APIs for:

- Authentication
- User management
- Profile management
- News retrieval
- Search
- NLP analysis
- Sentiment analysis
- NER
- Keyword extraction
- Topic analysis
- Trend analysis
- Admin operations

Uvicorn is used to run the Python API application.

### Example API Response Concept

```json
{
  "sentiment": {
    "label": "NEGATIVE",
    "confidence": 0.61
  },
  "entities": [
    {
      "word": "Example",
      "label": "PERSON"
    }
  ]
}
```

---

## Authentication

TrendVista uses secure authentication mechanisms including:

- Password hashing with bcrypt
- JWT access tokens
- Protected routes
- Token validation middleware
- Role-based access for administrative functionality

Authentication flow:

```text
User
 ↓
Login/Register
 ↓
Backend Authentication API
 ↓
Password Verification
 ↓
JWT Token
 ↓
Protected API Requests
 ↓
Authorized Response
```

---

## Dashboards and User Features

### Home Dashboard

Displays recent and trending articles with categories and search.

### Raw Text Analysis

Users can enter text and receive:

- Sentiment result
- Sentiment confidence
- Named entities

### Article Comparison

Users can compare two articles and inspect:

- Article overview
- Sentiment
- Keywords
- Similarity/related information

### Bookmark

Users can save news articles for later reading.

### Trending Topics

The system displays:

- Trending keywords
- Detected topics
- Trending articles
- Topic groups

### Sentiment Dashboard

Displays:

- Top trending topics
- Sentiment distribution
- Sentiment trend over time
- Time-range based analysis

### Geo-Tagging Dashboard

Provides geographical insights from news articles using location information and map visualization.

The documentation shows metrics such as total articles, geo-tagged articles, coverage, and unique locations.

### Admin Dashboard

Provides:

- Total users
- Admin users
- Regular users
- System status
- System health
- Advanced analytics
- User management

---

## Implementation

### Project Setup

The documented setup uses Python, FastAPI-related backend tooling, Supabase, Node.js, and React.js.

Example backend dependencies include:

```bash
pip install fastapi uvicorn python-dotenv sqlalchemy passlib[bcrypt] python-jose
pip install spacy nltk transformers keybert
```

Frontend dependencies include:

```bash
npm install react react-dom
npm install axios
npm install react-router-dom
npm install lucide-react
npm install framer-motion
```

### Frontend Setup

```bash
npx create-react-app trendvista-client
```

Then install the required dependencies and configure Tailwind CSS.

### Backend Setup

Create a virtual environment and configure environment variables in `.env`.

Example:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Run the API with Uvicorn:

```bash
uvicorn main:app --reload
```

> Adjust the module name if your project uses a different FastAPI entry file.

### Frontend Run

```bash
npm start
```

---

## Project Structure

A recommended repository structure is:

```text
TrendVista/
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── README.md
│
├── backend/
│   ├── app/
│   ├── models/
│   ├── routes/
│   ├── services/
│   ├── nlp/
│   ├── requirements.txt
│   └── main.py
│
├── docs/
│   └── Trendvista Documentation Final.docx
│
├── screenshots/
│   ├── login.png
│   ├── dashboard.png
│   ├── text-analysis.png
│   ├── trending.png
│   ├── admin-dashboard.png
│   └── geo-dashboard.png
│
├── .env.example
├── .gitignore
└── README.md
```

Do **not** upload real API keys, passwords, JWT secrets, database passwords, or other credentials.

---

## Testing

Testing covers functional and non-functional validation.

### Functional Testing

The documented test scope includes:

- User authentication
- Data ingestion
- Sentiment analysis
- Named Entity Recognition
- Topic modeling
- Trend detection
- Geo-tagging
- Bookmarks
- Article comparison
- Voice search
- Admin dashboard

### Non-Functional Testing

- API response performance
- ML inference speed
- JWT security
- Route protection
- UI/UX
- Error handling
- Input validation
- Scalability

### Testing Types

#### Unit Testing

Individual modules such as:

- JWT authentication
- NLP preprocessing
- Sentiment scoring
- NER extraction
- API endpoints

#### Integration Testing

Checks communication between:

```text
Frontend → Backend API
Backend → Database
NLP Engine → Topic Modeling → Trend Graphs
Geo-tagging → Leaflet Heatmap
```

#### System Testing

End-to-end workflows such as:

```text
Login
  ↓
Dashboard
  ↓
Trending Topics
  ↓
Detailed Analysis
```

and:

```text
Voice Search
  ↓
Speech-to-Text
  ↓
Keyword Search
  ↓
News Display
```

#### Black Box Testing

Tests system behavior without inspecting internal implementation.

Examples:

- Valid and invalid inputs
- Empty search
- Invalid JWT
- Missing network connection
- Invalid news source

#### White Box Testing

Evaluates internal logic including:

- Conditional flows
- Error handlers
- Token verification
- ML transformation
- Trend spike detection

#### User Acceptance Testing

The documentation validates:

- Accessibility
- Voice search
- Trend visualization
- Sentiment interpretation
- Dashboard navigation
- UI improvements
- Category grouping
- Responsive heatmaps

---

## Requirement Traceability

The documentation maps requirements to test cases, including:

| Requirement | Description | Test Cases |
|---|---|---|
| REQ-001 | User registration | TC001 |
| REQ-002 | Email validation | TC002 |
| REQ-003 | User login | TC003 |
| REQ-004 | Invalid login handling | TC004 |
| REQ-005 | Trending news load | TC005, TC006 |
| REQ-006 | API failure handling | TC006 |
| REQ-007 | Save bookmark | TC007 |
| REQ-008 | Remove bookmark | TC008 |
| REQ-009 | Search articles | TC009, TC010 |
| REQ-010 | Profile update | TC011 |
| REQ-011 | Compare articles | TC012 |

---

## Future Enhancements

The project documentation identifies the following future improvements:

### 1. Fake News and Misinformation Detection

Add fact-checking APIs or NLP-based credibility scoring to identify potentially misleading or biased content.

### 2. Social Media Integration

Integrate sources such as X/Twitter, Reddit, and LinkedIn to compare media trends with public sentiment.

### 3. User Feedback and Engagement

Allow users to rate or provide feedback on news accuracy and relevance.

### 4. Geo-Tagging and Location-Based Trend Analysis

Expand geographical analysis with heatmaps and interactive maps.

### 5. AI-Powered News Summarization

Use models such as BART or T5 to generate concise summaries of long articles.

### 6. Collaborative Research Portal

Allow journalists, researchers, and analysts to collaborate on trend findings and share datasets, graphs, and summaries.

---

## Conclusion

TrendVista demonstrates the integration of modern web technologies with Natural Language Processing to create an intelligent and user-centric news analytics platform.

The project transforms large volumes of unstructured news data into organized insights such as:

- Sentiment scores
- Trending topics
- Keyword summaries
- Named entities
- Time-based trends

The project applies full-stack development, database design, API integration, authentication, NLP model implementation, topic modeling, data visualization, and deployment practices.

The modular architecture covers authentication, NLP analysis, topic modeling and trend detection, and administration. These modules support scalability, maintainability, secure user interaction, and analytical outputs.

TrendVista provides a foundation for future features including multilingual support, fake-news detection, AI summarization, mobile integration, and real-time monitoring.

---

## Documentation

The repository can contain the complete project documentation separately:

```text
docs/
└── Trendvista Documentation Final.docx
```

The `README.md` should act as the quick project guide, while the complete 36-page report can be kept under `docs/`.

---

## Team

**Project:** TrendVista – Global News Trend Analyzer Using AI

**Internship:** Infosys Springboard Internship 6.0

**Team:** Team 2

**Mentor:** Mrs. P. Sathya

**Team Members:**
- Bille Arun Kumar
- Safira Farheen
- Akshay Kumar
- Shalini Gastagar
- Aditya Ghale

---

## Keywords

`TrendVista` `AI` `NLP` `News Analytics` `React.js` `FastAPI` `Python` `PostgreSQL` `Supabase` `Sentiment Analysis` `NER` `BERTopic` `KeyBERT` `Topic Modeling` `Trend Detection` `REST API` `JWT` `Tailwind CSS` `Data Visualization`
