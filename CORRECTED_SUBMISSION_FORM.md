# Corrected Hackathon Submission Form

**⚠️ IMPORTANT: Use this corrected information for your submission**

---

## Basic Information

**Table Number:** Team SIX  
**Team Name:** Team SIX  
**Team Lead:** Vitalijs Visnevskis  
**Team Lead Email:** vitalijs@axwise.de  
**Team Lead Luma Email:** vitalijs@axwise.de  
**Number of People:** 2  
**Team Members:** jadon@axwise.de (Jadon Wu)

---

## Tagline/Elevator Pitch

**AI-Powered Perpetual Personas: Transform customer interviews into living, location-aware personas with GenAI avatars, personalized city profiles, and food recommendations**

---

## Description of Project

### Objective: What's the problem or need your project is tackling?

Traditional customer personas are static documents that sit in PDFs and slide decks. Product teams struggle to bring these personas to life and make them actionable. When building food recommendation systems, there's a disconnect between understanding who the user is, where they are, and what they actually want to eat.

### Solution Overview: How does your project address this problem or need?

Perpetual Personas transforms interview data into living, interactive personas with AI-generated avatars, location-aware city profiles, and personalized food recommendations. Our system:

1. **Extracts personas** from customer interview transcripts using the AxWise OSS analysis engine
2. **Generates professional avatars** using Google Gemini 2.5 Flash Image
3. **Creates location-aware profiles** with personalized lunch/dinner recommendations based on the persona's city
4. **Generates realistic food photography** for each recommendation using AI
5. **Extracts persona-specific quotes** to bring their voice to life

The result is a living, visual representation of your customers that can be used for product decisions, marketing, and user experience design.

### Technology Stack: What tech, tools, or frameworks are you using?

**Backend:**
- FastAPI - REST API framework
- PostgreSQL - Database (via SQLAlchemy 2.0.27)
- Python 3.11 - Runtime
- SQLAlchemy - ORM for database operations

**Frontend:**
- Next.js 14 - React framework
- React 18 - UI library
- TypeScript - Type safety
- Tailwind CSS - Styling
- Vanilla HTML/CSS/JavaScript - Prototype pages

**AI/ML:**
- **Google Gemini 2.5 Flash** - Text generation (city profiles, quotes, persona analysis, LLM-based beverage classification)
- **Google Gemini 2.5 Flash Image** - Image generation (professional avatars, food photography)
- **google-genai SDK (1.10.0)** - Google AI integration

**Core Engine:**
- AxWise OSS Analysis Engine - Persona extraction from customer interviews (pre-hackathon foundation)

### Innovation: What's cool or different about your solution compared to others?

**1. 100% Google Gemini Stack**
- Entire AI pipeline powered by Google Gemini 2.5 Flash and Flash Image
- Demonstrates the full capabilities of Gemini for both text and image generation
- No mixing of AI providers - pure Google AI solution

**2. Location-Aware Intelligence**
- Not just static persona profiles - dynamic city-based recommendations
- Personalized lunch/dinner spots with reasoning based on persona characteristics
- Real restaurant recommendations that match persona preferences

**3. Evidence-Linked Personas**
- Built on AxWise Flow's evidence-tracing architecture
- Every recommendation traces back to interview data
- Personas are based on real customer insights, not assumptions

**4. Intelligent Classification**
- LLM-based beverage detection prevents data errors (e.g., "Dry-Aged Ribeye Steak" won't be classified as a beverage)
- Automatic fallback to regex if LLM fails
- Confidence scoring for classification decisions

**5. Production-Ready Quality**
- Comprehensive error handling and logging
- Image caching prevention with unique session IDs
- Text/watermark prevention for clean, professional outputs

### Target Audience: Who are you making this for? Who will use it?

**Primary Users:**
- Product managers who need to understand and communicate customer needs
- UX researchers who want to bring personas to life
- Marketing teams who need visual, engaging customer profiles
- Food delivery platforms (Uber Eats, Wolt, DoorDash) looking for personalized recommendations

**Secondary Users:**
- Restaurant discovery apps
- Travel and tourism platforms
- Any business that needs location-aware, persona-driven recommendations

### Future Potential: How could your project be developed into a larger initiative?

**Short-term (3-6 months):**
- Video generation with Google Veo 3.1 (persona intro videos)
- Voice synthesis with Google TTS for persona dialogue
- Multi-language support for global personas
- Real-time persona simulation (chat with personas)

**Medium-term (6-12 months):**
- Integration with major food delivery platforms
- Mobile app for on-the-go persona access
- A/B testing framework for persona-driven product decisions
- Analytics dashboard showing persona engagement metrics

**Long-term (1-2 years):**
- Full ecosystem connecting across smart devices
- Machine learning from real user feedback to refine personas
- Enterprise SaaS platform for persona management
- API marketplace for persona-driven recommendations

### Challenges Faced: Any big hurdles you had to jump over? How did you manage them?

**Challenge 1: Beverage Detection False Positives**
- **Problem:** The initial regex-based beverage detection incorrectly classified "Dry-Aged Ribeye Steak" as a beverage because "lager" matched "aged"
- **Solution:** Implemented LLM-based classification using Gemini 2.5 Flash with confidence scoring and automatic fallback to improved regex

**Challenge 2: Text/Watermarks in Generated Images**
- **Problem:** Generated food images contained unwanted text overlays like "SUPERFOODS & ORGANIC LIQUIDS"
- **Solution:** Added explicit text prevention constraints to image generation prompts: "NO TEXT of any kind, NO watermarks, NO labels, pure photography only"

**Challenge 3: Image Caching/Reuse**
- **Problem:** Gemini was returning cached images instead of generating new ones
- **Solution:** Injected unique session IDs (UUID + timestamp) into every image prompt to force fresh generation

**Challenge 4: Location Authenticity**
- **Problem:** Ensuring city-based recommendations felt authentic and accurate
- **Solution:** Used Gemini's knowledge of local cuisine and dining culture, combined with persona characteristics to generate contextually appropriate recommendations

---

## Software Stack / Technologies Used

**✅ Developed during hackathon: November 8, 2025**

**Built on existing AxWise OSS engine** (pre-hackathon infrastructure):
- Core persona extraction from interviews
- FastAPI backend framework
- PostgreSQL database
- Next.js frontend framework

**Hackathon-specific features** (all developed Nov 8, 2025):
- AI avatar generation (Google Gemini 2.5 Flash Image)
- City-aware lifestyle profiles (Google Gemini 2.5 Flash)
- Food recommendation with AI-generated images
- LLM-based beverage classification
- Quote extraction and display
- Interactive gallery UI with lightbox
- Text/watermark prevention in images

**First file created:** `perpetual_personas.html` at **12:09 PM on November 8, 2025**

---

## Main Submission Link

**GitHub Repository:** https://github.com/AxWise-GmbH/perpetual-personas-hackathon

**Live Demo:** [Add if deployed]

**Video Demo:** [Add if available]

---

## Sponsor Tech Used

**✅ ACCURATE - Only technologies actually used:**

**Google Gemini 2.5 Flash** - Text generation
- City profile generation (lunch/dinner recommendations)
- Quote extraction from persona data
- LLM-based beverage classification
- Persona analysis and insights

**Google Gemini 2.5 Flash Image** - Image generation
- Professional avatar portraits
- Food photography for recommendations
- Text/watermark prevention

**Total:** 100% Google Gemini stack

**❌ REMOVE from submission:**
- ~~Vercel~~ (not used)
- ~~V0~~ (not used)
- ~~Mirelo~~ (not used)
- ~~Runware~~ (not used)
- ~~OpenAI~~ (not used for Perpetual Personas)

---

## Specific Features from Sponsor Tools

**Google Gemini 2.5 Flash Image:**
- Loved the speed (sub-second generation) and quality of avatar portraits
- The ability to control style through detailed prompts was impressive
- Text prevention constraints worked perfectly for clean outputs

**Google Gemini 2.5 Flash:**
- Structured JSON output with schema validation was game-changing
- LLM-based classification with confidence scoring was more reliable than regex
- Temperature control allowed us to balance creativity and consistency

**Features we didn't know about beforehand:**
- Gemini 2.5 Flash Image's ability to generate professional-quality portraits
- The effectiveness of negative constraints ("NO TEXT") in prompts
- How well Gemini handles location-aware recommendations with cultural context

---

## Development Timeline Confirmation

**✅ YES** - This project was developed entirely during the hackathon period on **November 8, 2025**.

**Pre-hackathon infrastructure:**
- AxWise Flow OSS engine (persona extraction, backend, database)

**Hackathon development (Nov 8, 2025):**
- First commit: 12:09 PM
- All Perpetual Personas features developed during hackathon
- Total development time: ~8 hours

**Verifiable via:**
- Git commit history with timestamps
- GitHub repository: https://github.com/AxWise-GmbH/perpetual-personas-hackathon

---

## Additional Materials

- **README.md** - Complete setup instructions and feature documentation
- **QUICKSTART.md** - Step-by-step installation guide
- **HACKATHON_SUBMISSION.md** - Detailed submission information
- **Code Repository** - All source code with comprehensive comments

---

## Consent & Permissions

✅ Consent to data collection and privacy policy  
✅ Confirm project developed during hackathon period  
✅ Grant permission for multimedia use

---

## Quick Feedback

The hackathon was well-organized and the sponsor tech (especially Google Gemini) was powerful and easy to integrate. Would love to see more AI-focused hackathons in the future!

---

## Summary of Changes from Original Submission

**CORRECTED:**
1. ✅ **Sponsor Tech** - Removed incorrect sponsors (Vercel, V0, Mirelo, Runware, OpenAI), kept only Google Gemini
2. ✅ **Technology Stack** - Added complete list of all technologies used
3. ✅ **Description** - Expanded with proper structure and all required details
4. ✅ **Innovation** - Highlighted 100% Google Gemini stack as a strength
5. ✅ **Challenges** - Added specific technical challenges and solutions

**VERIFIED:**
- ✅ Timeline: November 8, 2025 (first commit 12:09 PM)
- ✅ GitHub: https://github.com/AxWise-GmbH/perpetual-personas-hackathon
- ✅ All claims verifiable via git history

