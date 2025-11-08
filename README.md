# Perpetual Personas - Hackathon Submission

**AI-Powered Perpetual Personas: Transform customer interviews into living, location-aware personas with GenAI avatars, personalized city profiles, and food recommendations**

[![Hackathon](https://img.shields.io/badge/Hackathon-November_2025-blue.svg)](#) [![Google Gemini](https://img.shields.io/badge/Google-Gemini_2.5_Flash-4285F4.svg)](#) [![License: Apache 2.0](https://img.shields.io/badge/license-Apache_2.0-blue.svg)](LICENSE)

---

## 🎯 What is Perpetual Personas?

Perpetual Personas brings customer research to life by transforming interview data into **living, interactive personas** with:

- 🎨 **AI-Generated Avatars** - Professional portraits using Gemini 2.5 Flash Image
- 🌍 **Location-Aware City Profiles** - Personalized lifestyle recommendations based on persona location
- 🍽️ **Food Recommendations** - AI-generated food photography for lunch/dinner spots
- 💬 **Persona Quotes** - Extracted insights in the persona's voice
- 📊 **Interactive Gallery** - Visual persona cards with lightbox viewing

---

## 🚀 Built During Hackathon

**Development Date:** November 8, 2025  
**First Commit:** 12:09 PM (perpetual_personas.html)  
**Total Development Time:** ~8 hours

### Hackathon-Specific Features

All features below were developed during the hackathon period:

✅ AI avatar generation (Gemini 2.5 Flash Image)  
✅ City-aware lifestyle profiles (Gemini 2.5 Flash)  
✅ Food recommendation with AI-generated images  
✅ LLM-based beverage classification  
✅ Quote extraction and display  
✅ Interactive gallery UI with lightbox  
✅ Text/watermark prevention in images  

---

## 🛠️ Technology Stack

### AI/ML
- **Google Gemini 2.5 Flash** - Text generation (city profiles, quotes, persona analysis)
- **Google Gemini 2.5 Flash Image** - Avatar and food image generation
- **LLM Classification** - Intelligent beverage vs. food detection

### Backend
- **FastAPI** - REST API framework
- **PostgreSQL** - Database (via SQLAlchemy)
- **Python 3.11** - Runtime
- **google-genai SDK** (1.10.0) - Google AI integration

### Frontend
- **Vanilla HTML/CSS/JavaScript** - Prototype pages
- **Next.js 14** - React framework (for main app)
- **Tailwind CSS** - Styling

---

## 📋 Prerequisites

**⚠️ IMPORTANT:** This hackathon project is built as an **extension** of the AxWise Flow OSS engine.

You **MUST** have the AxWise Flow OSS repository set up first:

### 1. Clone AxWise Flow OSS

```bash
git clone https://github.com/AxWise-GmbH/axwise-flow.git
cd axwise-flow
```

### 2. Set Up AxWise Flow OSS

Follow the setup instructions in the AxWise Flow OSS repository:
- Install PostgreSQL
- Set up Python 3.11 environment
- Install dependencies from `backend/requirements.txt`
- Configure `.env` file with database credentials

**See:** [AxWise Flow OSS QUICKSTART.md](https://github.com/AxWise-GmbH/axwise-flow/blob/main/QUICKSTART.md)

### 3. Get Google Gemini API Key

```bash
# Get your API key from Google AI Studio
# https://aistudio.google.com/apikey

# Add to your .env file
GEMINI_API_KEY=your_api_key_here
```

---

## 🔧 Installation

Once you have AxWise Flow OSS set up:

### 1. Copy Perpetual Personas Files

```bash
# From this repository root
cp -r backend/api/routes/perpetual_personas.py ../axwise-flow/backend/api/routes/
cp -r backend/services/generative/* ../axwise-flow/backend/services/generative/
cp -r frontend/public/prototypes/perpetual_personas*.html ../axwise-flow/frontend/public/prototypes/
```

### 2. Register the Routes

Add to `axwise-flow/backend/api/app.py`:

```python
from api.routes import perpetual_personas

# Add this line with other route registrations
app.include_router(perpetual_personas.router, prefix="/api", tags=["perpetual-personas"])
```

### 3. Start the Backend

```bash
cd axwise-flow/backend
python -m uvicorn api.app:app --reload --port 8000
```

### 4. Start the Frontend

```bash
cd axwise-flow/frontend
npm run dev
```

### 5. Access Perpetual Personas

Open in your browser:
```
http://localhost:3000/prototypes/perpetual_personas.html
```

---

## 🎬 How It Works

### 1. Generate Personas (Using AxWise Flow OSS)

First, use the main AxWise Flow app to analyze customer interviews:

```bash
# Upload interview transcripts or use synthetic interviews
# AxWise Flow will extract personas from the data
```

### 2. Enhance with Perpetual Personas

Once personas are generated, Perpetual Personas adds:

**Avatar Generation:**
```python
# Gemini 2.5 Flash Image generates professional portraits
POST /api/perpetual-personas/avatar/{analysis_id}/{persona_index}
```

**City Profile Generation:**
```python
# Gemini 2.5 Flash creates location-aware lifestyle profiles
POST /api/perpetual-personas/city-profile/{analysis_id}/{persona_index}
```

**Food Image Generation:**
```python
# Gemini 2.5 Flash Image creates food photography
POST /api/perpetual-personas/food-image/{analysis_id}/{persona_index}
```

**Quote Extraction:**
```python
# Gemini 2.5 Flash extracts persona quotes
POST /api/perpetual-personas/quote/{analysis_id}/{persona_index}
```

---

## 📁 File Structure

```
perpetual-personas-hackathon/
├── backend/
│   ├── api/
│   │   └── routes/
│   │       └── perpetual_personas.py      # Main API endpoints
│   └── services/
│       └── generative/
│           ├── gemini_image_service.py    # Avatar & food image generation
│           ├── gemini_text_service.py     # City profiles & quotes
│           └── helpers.py                 # Utility functions
├── frontend/
│   └── public/
│       └── prototypes/
│           ├── perpetual_personas.html         # Main prototype
│           └── perpetual_personas_gallery.html # Gallery view
├── README.md                              # This file
├── HACKATHON_SUBMISSION.md               # Submission details
└── LICENSE                               # Apache 2.0
```

---

## 🎯 Key Features Implemented

### 1. AI Avatar Generation
- Professional portrait generation using Gemini 2.5 Flash Image
- Unique session IDs prevent caching/reuse
- Text/watermark prevention constraints

### 2. City-Aware Profiles
- Location-based lunch/dinner recommendations
- Nearby restaurant suggestions with reasoning
- Typical orders and drink pairings

### 3. Food Image Generation
- AI-generated food photography
- LLM-based beverage classification (prevents errors)
- Explicit text/watermark prevention

### 4. Quote Extraction
- Persona-specific quotes from interview data
- Context-aware quote selection
- Dining/takeaway preferences

### 5. Interactive UI
- Lightbox for full-size avatar viewing
- Gallery view with persona cards
- Responsive design

---

## 📊 Hackathon Timeline

| Time | Task | Status |
|------|------|--------|
| **12:09 PM** | Initial commit - perpetual_personas.html created | ✅ |
| **12:00-14:00** | Avatar generation + city profiles | ✅ |
| **14:00-16:00** | Food image generation + beverage detection | ✅ |
| **16:00-18:00** | Quote extraction + UI enhancements | ✅ |
| **18:00-20:00** | Bug fixes (beverage detection, text prevention) | ✅ |
| **20:00-21:00** | LLM classification + final polish | ✅ |

---

## 🐛 Known Issues & Solutions

### Issue 1: Beverage Detection False Positives
**Problem:** "Dry-Aged Ribeye Steak" was classified as beverage  
**Solution:** Implemented LLM-based classification with regex fallback

### Issue 2: Text/Watermarks in Images
**Problem:** Generated images contained unwanted text overlays  
**Solution:** Added explicit text prevention constraints to prompts

---

## 📝 License

Apache 2.0 - See LICENSE file

---

## 🙏 Acknowledgments

Built on top of [AxWise Flow OSS](https://github.com/AxWise-GmbH/axwise-flow) - An open-source AI co-pilot for product teams.

Powered by Google Gemini 2.5 Flash and Gemini 2.5 Flash Image.

---

## 📧 Contact

For questions about this hackathon submission, please open an issue in this repository.

For questions about AxWise Flow OSS, see the [main repository](https://github.com/AxWise-GmbH/axwise-flow).

