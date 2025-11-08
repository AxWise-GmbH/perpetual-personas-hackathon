# Final Hackathon Submission - Perpetual Personas

**Team:** Team SIX  
**Date:** November 8, 2025  
**GitHub:** https://github.com/AxWise-GmbH/perpetual-personas-hackathon

---

## Tagline/Elevator Pitch

**AI-Powered Perpetual Personas: Transform customer interviews into living, location-aware personas with GenAI avatars, personalized city profiles, and food recommendations**

---

## Description of Project

### Objective: What's the problem or need your project is tackling?

Food recommendation based on persona context and location. Traditional customer personas are static documents that sit in PDFs and slide decks. Product teams struggle to bring these personas to life and make them actionable. When building food recommendation systems, there's a disconnect between understanding who the user is, where they are, and what they actually want to eat.

### Solution Overview: How does your project address this problem or need?

Our system starts with rich persona data to create digital avatars that represent different types of people and their preferences. It then connects those avatars to local spots that match their tastes and even generates realistic images of the food they might enjoy using Runware and Gemini 2.5 Nano Banana. These visuals and insights can be easily embedded into platforms like Uber Eats or Wolt to make recommendations more engaging and relevant.

The system:
1. **Extracts personas** from customer interview transcripts using the AxWise OSS analysis engine
2. **Generates professional avatars** using Runware and Gemini 2.5 Nano Banana
3. **Creates location-aware profiles** with personalized lunch/dinner recommendations based on the persona's city
4. **Generates realistic food photography** for each recommendation using AI
5. **Extracts persona-specific quotes** to bring their voice to life

### Innovation: What's cool or different about your solution compared to others?

What sets our project apart is how it blends context, personalization, and visual appeal. It doesn't just recommend food—it understands the person behind the choice, their surroundings, and what looks appetizing to them in that moment. The AI-generated food images using Runware and Gemini 2.5 Nano Banana make the experience more tempting.

**Key Innovations:**
- **OpenAI-Compatible Architecture:** Built with schema compatibility for seamless integration with multiple AI providers
- **Multi-Provider AI Stack:** Combines OpenAI, Google Gemini, Runware for optimal results
- **Location-Aware Intelligence:** Dynamic city-based recommendations that match persona preferences
- **Evidence-Linked Personas:** Every recommendation traces back to real interview data
- **Intelligent Classification:** LLM-based beverage detection prevents data errors
- **Production-Ready Quality:** Comprehensive error handling, image caching prevention, text/watermark prevention

### Target Audience: Who are you making this for? Who will use it?

We're building this for food delivery platforms, restaurant finders, and food tech companies that want to offer smarter, more personal recommendations. It also serves end users who love getting food suggestions that actually match their vibe, location, and cravings.

**Primary Users:**
- Product managers who need to understand and communicate customer needs
- UX researchers who want to bring personas to life
- Marketing teams who need visual, engaging customer profiles
- Food delivery platforms (Uber Eats, Wolt, DoorDash) looking for personalized recommendations

### Technical Stack: What tech, tools, or frameworks are you using?

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
- **OpenAI** - Schema-compatible architecture for seamless integration
- **Google Gemini 2.5 Flash** - Text generation (city profiles, quotes, beverage classification, persona analysis)
- **Runware** - Image generation infrastructure
- **Gemini 2.5 Nano Banana** - Image generation model (avatars, food photography)
- **Runware** - Video generation capability for future persona intro videos
- **google-genai SDK (1.10.0)** - Google AI integration

**Core Engine:**
- AxWise OSS Analysis Engine - Persona extraction from customer interviews (pre-hackathon foundation)

### Future Potential: How could your project be developed into a larger initiative?

This could evolve into a full ecosystem that connects across smart devices, like recommending meals through your mobile assistant. We plan to integrate Runware for persona intro videos. Over time, the system could learn from real feedback to refine its suggestions automatically.

**Short-term (3-6 months):**
- Video generation with Runware for persona intro videos
- Voice synthesis for persona dialogue
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

One of the toughest parts was generating food images that looked realistic and matched each person's preferences using Runware and Gemini 2.5 Nano Banana. We built an OpenAI-compatible connector to make the integration seamless. Another challenge was making sure the location-based recommendations felt authentic and accurate.

**Specific Technical Challenges:**

**Challenge 1: Beverage Detection False Positives**
- **Problem:** Initial regex-based beverage detection incorrectly classified "Dry-Aged Ribeye Steak" as a beverage
- **Solution:** Implemented LLM-based classification using Gemini 2.5 Flash with confidence scoring and automatic fallback

**Challenge 2: Text/Watermarks in Generated Images**
- **Problem:** Generated food images contained unwanted text overlays
- **Solution:** Added explicit text prevention constraints to Runware/Gemini prompts: "NO TEXT of any kind, NO watermarks, pure photography only"

**Challenge 3: Multi-Provider Integration**
- **Problem:** Integrating OpenAI, Gemini, and Runware with consistent interfaces
- **Solution:** Built OpenAI-compatible schema layer for seamless provider switching

**Challenge 4: Image Caching/Reuse**
- **Problem:** AI was returning cached images instead of generating new ones
- **Solution:** Injected unique session IDs (UUID + timestamp) into every image prompt

---

## Software Stack / Technologies Used

**✅ Developed during hackathon: November 8, 2025**

**Built on existing AxWise OSS engine** (pre-hackathon infrastructure):
- Core persona extraction from interviews
- FastAPI backend framework
- PostgreSQL database
- Next.js frontend framework

**Hackathon-specific features** (all developed Nov 8, 2025):
- AI avatar generation (Runware & Gemini 2.5 Nano Banana)
- City-aware lifestyle profiles (Google Gemini 2.5 Flash)
- Food recommendation with AI-generated images
- OpenAI-compatible architecture
- LLM-based beverage classification
- Quote extraction and display
- Interactive gallery UI with lightbox
- Text/watermark prevention in images

**First file created:** `perpetual_personas.html` at **12:09 PM on November 8, 2025**

---

## Sponsor Tech Used

**OpenAI** - Schema-compatible architecture for seamless AI provider integration

**Google Gemini 2.5 Flash** - Text generation
- City profile generation (lunch/dinner recommendations)
- Quote extraction from persona data
- LLM-based beverage classification
- Persona analysis and insights

**Runware** - Image generation infrastructure

**Gemini 2.5 Nano Banana** - Image generation model
- Professional avatar portraits
- Food photography for recommendations
- Text/watermark prevention


---

## Specific Features from Sponsor Tools

**Runware & Gemini 2.5 Nano Banana:**
- Loved the "Nano Banana" model for fast, high-quality image generation
- Sub-second generation times for avatars and food photography
- Excellent quality for professional portraits and food photography
- OpenAI-compatible schema made integration seamless

**Google Gemini 2.5 Flash:**
- Structured JSON output with schema validation was game-changing
- LLM-based classification with confidence scoring was more reliable than regex
- Temperature control allowed us to balance creativity and consistency
- Excellent location-aware recommendations with cultural context


**Features we didn't know about beforehand:**
- Gemini 2.5 Nano Banana's ability to generate professional-quality portraits
- The effectiveness of negative constraints ("NO TEXT") in prompts
- How well Gemini handles location-aware recommendations with cultural context
- Runware's speed and quality for food photography

---

## Links

**GitHub Repository:** https://github.com/AxWise-GmbH/perpetual-personas-hackathon

**Main Submission Link:** https://github.com/AxWise-GmbH/perpetual-personas-hackathon

---

## Development Timeline

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

## Team Information

**Team Name:** Team SIX  
**Team Lead:** Vitalijs Visnevskis (vitalijs@axwise.de)  
**Team Members:** Jadon Wu (jadon@axwise.de)  
**Table Number:** Team SIX

---

## Consent & Permissions

✅ Consent to data collection and privacy policy  
✅ Confirm project developed during hackathon period  
✅ Grant permission for multimedia use

---



