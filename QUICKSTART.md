# Perpetual Personas - Quick Start Guide

**⚠️ IMPORTANT:** This project requires AxWise Flow OSS to be set up first!

---

## Prerequisites

### 1. Install AxWise Flow OSS

```bash
# Clone the main repository
git clone https://github.com/AxWise-GmbH/axwise-flow.git
cd axwise-flow

# Follow the setup instructions in QUICKSTART.md
# This includes:
# - PostgreSQL installation
# - Python 3.11 environment
# - Backend dependencies
# - Database setup
```

### 2. Get Google Gemini API Key

```bash
# Visit Google AI Studio
# https://aistudio.google.com/apikey

# Add to axwise-flow/backend/.env
GEMINI_API_KEY=your_api_key_here
```

---

## Installation

### Step 1: Copy Perpetual Personas Files

```bash
# From the perpetual-personas-hackathon directory
cd /path/to/perpetual-personas-hackathon

# Copy backend files
cp backend/api/routes/perpetual_personas.py ../axwise-flow/backend/api/routes/
cp backend/services/generative/gemini_image_service.py ../axwise-flow/backend/services/generative/
cp backend/services/generative/gemini_text_service.py ../axwise-flow/backend/services/generative/
cp backend/services/generative/helpers.py ../axwise-flow/backend/services/generative/

# Copy frontend files
cp frontend/public/prototypes/perpetual_personas.html ../axwise-flow/frontend/public/prototypes/
cp frontend/public/prototypes/perpetual_personas_gallery.html ../axwise-flow/frontend/public/prototypes/
```

### Step 2: Register Routes in AxWise Flow

Edit `axwise-flow/backend/api/app.py`:

```python
# Add this import at the top
from api.routes import perpetual_personas

# Add this line with other route registrations (around line 50-60)
app.include_router(perpetual_personas.router, prefix="/api", tags=["perpetual-personas"])
```

### Step 3: Verify Dependencies

```bash
cd axwise-flow/backend

# Check if google-genai is installed
pip list | grep google-genai

# If not installed:
pip install google-genai>=1.10.0
```

---

## Running the Application

### Start Backend

```bash
cd axwise-flow/backend
python -m uvicorn api.app:app --reload --port 8000
```

**Expected output:**
```
INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
INFO:     Started reloader process
INFO:     Started server process
INFO:     Waiting for application startup.
INFO:     Application startup complete.
```

### Start Frontend

```bash
cd axwise-flow/frontend
npm run dev
```

**Expected output:**
```
ready - started server on 0.0.0.0:3000, url: http://localhost:3000
```

---

## Access Perpetual Personas

### Option 1: Direct Prototype Access

Open in your browser:
```
http://localhost:3000/prototypes/perpetual_personas.html
```

### Option 2: Gallery View

```
http://localhost:3000/prototypes/perpetual_personas_gallery.html
```

---

## Usage Flow

### 1. Create Analysis with Personas

First, use the main AxWise Flow app to create an analysis:

```bash
# Open the main app
http://localhost:3000

# Upload interview transcripts or use synthetic interviews
# AxWise Flow will extract personas from the data
# Note the analysis_id from the URL
```

### 2. Generate Avatar

In the Perpetual Personas prototype:
1. Enter the `analysis_id` from step 1
2. Select persona index (0, 1, 2, etc.)
3. Click "Generate Avatar"
4. Wait ~2-3 seconds for Gemini 2.5 Flash Image to generate

### 3. Generate City Profile

1. Select a city (Berlin, London, Paris, etc.)
2. Click "Generate City Profile"
3. Wait ~3-5 seconds for Gemini 2.5 Flash to generate
4. View lunch/dinner recommendations

### 4. Generate Food Images

1. Click on any food image placeholder
2. Wait ~2-3 seconds for Gemini 2.5 Flash Image to generate
3. View AI-generated food photography

### 5. Extract Quote

1. Click "Generate Quote"
2. Wait ~2-3 seconds for Gemini 2.5 Flash to extract
3. View persona-specific quote

---

## API Endpoints

All endpoints are available at `http://localhost:8000/api/`

### Avatar Generation
```bash
POST /api/perpetual-personas/avatar/{analysis_id}/{persona_index}
```

### City Profile Generation
```bash
POST /api/perpetual-personas/city-profile/{analysis_id}/{persona_index}
Body: {"city": "Berlin"}
```

### Food Image Generation
```bash
POST /api/perpetual-personas/food-image/{analysis_id}/{persona_index}
Body: {
  "restaurant_name": "Grill Royal",
  "dish": "Dry-Aged Ribeye Steak",
  "meal_type": "dinner",
  "recommendation_index": 0
}
```

### Quote Extraction
```bash
POST /api/perpetual-personas/quote/{analysis_id}/{persona_index}
```

---

## Troubleshooting

### Issue: "Module not found: api.routes.perpetual_personas"

**Solution:** Make sure you copied the files to the correct location and registered the routes in `app.py`

### Issue: "GEMINI_API_KEY not found"

**Solution:** Add your Gemini API key to `axwise-flow/backend/.env`:
```bash
GEMINI_API_KEY=your_api_key_here
```

### Issue: "Analysis not found"

**Solution:** Create an analysis first using the main AxWise Flow app before using Perpetual Personas

### Issue: "Persona index out of range"

**Solution:** Check how many personas were generated in your analysis. Index starts at 0.

---

## Testing

### Quick Test

```bash
# 1. Start backend
cd axwise-flow/backend
python -m uvicorn api.app:app --reload --port 8000

# 2. In another terminal, test avatar generation
curl -X POST http://localhost:8000/api/perpetual-personas/avatar/1/0

# Expected: JSON response with base64 avatar image
```

---

## Next Steps

1. ✅ Set up AxWise Flow OSS
2. ✅ Copy Perpetual Personas files
3. ✅ Register routes
4. ✅ Start backend and frontend
5. ✅ Create an analysis with personas
6. ✅ Generate avatars, city profiles, and food images
7. 🎉 Enjoy your living, location-aware personas!

---

## Support

- **AxWise Flow OSS Issues:** https://github.com/AxWise-GmbH/axwise-flow/issues
- **Perpetual Personas Issues:** [This repository's issues]
- **Google Gemini Docs:** https://ai.google.dev/gemini-api/docs

---

## License

Apache 2.0 - See LICENSE file

