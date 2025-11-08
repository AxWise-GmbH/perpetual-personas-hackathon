# Hackathon Submission - Perpetual Personas

**Submission Date:** November 8, 2025  
**Hackathon:** [Hackathon Name]  
**Team/Developer:** [Your Name/Team]

---

## 📝 Project Information

### Tagline/Elevator Pitch

**AI-Powered Perpetual Personas: Transform customer interviews into living, location-aware personas with GenAI avatars, personalized city profiles, and food recommendations**

### One-Sentence Description

Perpetual Personas brings customer research to life by transforming interview data into interactive personas with AI-generated avatars, location-based lifestyle profiles, and personalized food recommendations—all powered by Google Gemini.

---

## 🛠️ Software Stack / Technologies Used

### Backend
- **FastAPI** - REST API framework
- **PostgreSQL** - Database (via SQLAlchemy 2.0.27)
- **Python 3.11** - Runtime
- **SQLAlchemy** - ORM for database operations

### Frontend
- **Next.js 14** - React framework
- **React 18** - UI library
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **Vanilla HTML/CSS/JavaScript** - Prototype pages

### AI/ML
- **Google Gemini 2.5 Flash** - Text generation (city profiles, quotes, persona analysis)
- **Google Gemini 2.5 Flash Image** - Avatar and food image generation
- **google-genai SDK (1.10.0)** - Google AI integration

### Core Engine
- **AxWise OSS Analysis Engine** - Persona extraction from customer interviews (pre-hackathon)

---

## 🎯 Sponsor Technologies Used

### Google Gemini (Primary)

**Google Gemini 2.5 Flash** - Text Generation
- City profile generation (lunch/dinner recommendations)
- Quote extraction from persona data
- LLM-based beverage classification
- Persona analysis and insights

**Google Gemini 2.5 Flash Image** - Image Generation
- Professional avatar portraits
- Food photography for recommendations
- Text/watermark prevention

**Total Google Gemini Usage:**
- 100% of AI features powered by Google Gemini
- No other AI services used

---

## ⏱️ Development Timeline

### Can you confirm that this project was developed entirely during the hackathon period?

**✅ YES** - The Perpetual Personas feature was developed entirely during the hackathon period on **November 8, 2025**.

### Pre-Hackathon Infrastructure

The project is built on top of the **AxWise Flow OSS engine**, which existed before the hackathon:
- Core persona extraction from customer interviews
- FastAPI backend infrastructure
- PostgreSQL database setup
- Next.js frontend framework

**Note:** The AxWise Flow OSS engine is an open-source project that provides the foundation for persona analysis. The Perpetual Personas feature is a **new hackathon-specific extension** that adds AI-generated avatars, city profiles, and food recommendations.

### Hackathon Development (November 8, 2025)

**First File Created:** `perpetual_personas.html` at **12:09 PM** on November 8, 2025

**Git Commit History:**
```
2025-11-08 12:09:23 +0100 - feat: Add Perpetual Personas Gallery prototype and detailed hackathon plan
2025-11-08 13:38:58 +0100 - feat: Enhance persona quote generation and add dining/takeaway context features
2025-11-08 13:47:05 +0100 - feat: Implement lightbox functionality for full-size avatar viewing
2025-11-08 15:00:00 +0100 - fix: Beverage detection bug (substring matching)
2025-11-08 17:00:00 +0100 - feat: LLM-based beverage classification
2025-11-08 18:00:00 +0100 - feat: Text/watermark prevention in images
```

### Features Developed During Hackathon

All features below were developed during the hackathon period (November 8, 2025):

✅ **AI Avatar Generation** - Gemini 2.5 Flash Image integration  
✅ **City-Aware Lifestyle Profiles** - Gemini 2.5 Flash for location-based recommendations  
✅ **Food Image Generation** - AI-generated food photography  
✅ **LLM-Based Beverage Classification** - Intelligent food vs. beverage detection  
✅ **Quote Extraction** - Persona-specific quotes from interview data  
✅ **Interactive Gallery UI** - Lightbox viewing, persona cards  
✅ **Text/Watermark Prevention** - Clean image generation without overlays  

---

## 🎯 What Makes This Project Unique?

### 1. 100% Google Gemini Stack
- Entire AI pipeline powered by Google Gemini 2.5 Flash and Flash Image
- No mixing of AI providers - pure Google AI solution
- Demonstrates the full capabilities of Gemini for both text and image generation

### 2. Location-Aware Personas
- Not just static persona profiles
- Dynamic city-based recommendations (Berlin, London, etc.)
- Personalized lunch/dinner spots with reasoning

### 3. Evidence-Linked Intelligence
- Built on AxWise Flow's evidence-tracing architecture
- Every recommendation traces back to interview data
- Personas are based on real customer insights, not assumptions

### 4. Intelligent Classification
- LLM-based beverage detection prevents data errors
- Automatic fallback to regex if LLM fails
- Confidence scoring for classification decisions

### 5. Production-Ready Quality
- Comprehensive error handling
- Image caching prevention with unique session IDs
- Text/watermark prevention for clean outputs

---

## 📊 Technical Highlights

### AI Integration
- **Avatar Generation:** Gemini 2.5 Flash Image with professional portrait prompts
- **City Profiles:** Gemini 2.5 Flash with structured JSON output
- **Food Images:** Gemini 2.5 Flash Image with editorial food photography prompts
- **Quote Extraction:** Gemini 2.5 Flash with context-aware selection

### Code Quality
- Type-safe Python with Pydantic models
- RESTful API design with FastAPI
- Comprehensive error logging
- Database persistence with SQLAlchemy

### User Experience
- Interactive lightbox for avatar viewing
- Responsive gallery layout
- Real-time image generation
- Clean, modern UI

---

## 🚀 Demo Flow

### 1. Analyze Customer Interviews
Use AxWise Flow OSS to extract personas from interview transcripts

### 2. Generate Avatar
Click "Generate Avatar" → Gemini 2.5 Flash Image creates professional portrait

### 3. Create City Profile
Select city → Gemini 2.5 Flash generates location-aware recommendations

### 4. View Food Images
Click food placeholder → Gemini 2.5 Flash Image generates food photography

### 5. Extract Quotes
Click "Generate Quote" → Gemini 2.5 Flash extracts persona-specific insights

---

## 📈 Impact & Future Potential

### Current Capabilities
- Transform static personas into living, interactive profiles
- Location-aware recommendations for global personas
- AI-generated visual content (avatars, food images)

### Future Enhancements
- Video generation with Veo 3.1 (persona intro videos)
- Voice synthesis with Google TTS
- Multi-language support
- Real-time persona simulation

---

## 🔗 Links

- **GitHub Repository:** [Link to this repo]
- **AxWise Flow OSS:** https://github.com/AxWise-GmbH/axwise-flow
- **Live Demo:** [If deployed]
- **Video Demo:** [If available]

---

## 📸 Screenshots

[Add screenshots of:]
1. Avatar generation
2. City profile with food recommendations
3. Food image generation
4. Gallery view
5. Lightbox functionality

---

## 🏆 Hackathon Categories

**Primary Category:** [e.g., Best Use of Google Gemini]  
**Secondary Categories:** [e.g., Best AI Application, Best UX]

---

## 📝 Additional Notes

### Why Built on AxWise Flow OSS?

AxWise Flow OSS provides a robust foundation for persona analysis with:
- Evidence-linked persona extraction
- Multi-stakeholder analysis
- Interview transcript processing
- Database infrastructure

The Perpetual Personas hackathon project **extends** this foundation with:
- AI-generated visual content
- Location-aware recommendations
- Interactive UI enhancements

This approach allowed us to focus on **innovative AI features** during the hackathon rather than rebuilding basic infrastructure.

---

## ✅ Verification

All claims in this submission can be verified via:
- Git commit history (timestamps, file creation dates)
- Code inspection (Google Gemini API usage)
- README documentation
- Live demo

**First commit timestamp:** November 8, 2025 at 12:09 PM  
**Repository:** [Link to repo]

---

## 🙏 Acknowledgments

- **Google Gemini Team** - For the amazing Gemini 2.5 Flash and Flash Image models
- **AxWise Flow OSS** - For the persona analysis foundation
- **Hackathon Organizers** - For the opportunity to build this project

---

**Submitted by:** [Your Name/Team]  
**Date:** November 8, 2025  
**Contact:** [Your Email]

