# Bharat Sahayak 🇮🇳

**Speak. Discover. Access.**

A voice-first, multilingual AI assistant helping Indian citizens access public services, education programs, government jobs, and local markets.

## Features

✅ **Voice-First Interface** - Speak in Hindi or English
✅ **Public Services** - Discover government schemes (PM-KISAN, Ayushman Bharat, etc.)
✅ **Education & Skills** - Find scholarships and skill development programs
✅ **Government Jobs** - Explore opportunities (SSC, Railway, Banking, UPSC, etc.)
✅ **Local Markets** - Find nearby wholesale markets
✅ **Accessibility** - Slow speech mode, simple explanations, high contrast UI
✅ **Mobile-First** - Optimized for low digital literacy users

## Tech Stack

- **Frontend**: Next.js 14, React, TypeScript
- **Styling**: Tailwind CSS
- **Animations**: Framer Motion
- **Voice**: Web Speech API (Speech Recognition & Synthesis)
- **Data**: Static JSON datasets

## Getting Started

### Prerequisites

- Node.js 18+ installed
- Modern browser (Chrome or Edge recommended for voice features)

### Installation

1. Install dependencies:
```bash
npm install
```

2. Run the development server:
```bash
npm run dev
```

3. Open [http://localhost:3000](http://localhost:3000) in your browser

## Usage

1. **Select Language** - Choose Hindi or English
2. **Pick a Category** - Tap on Public Services, Education, Jobs, or Markets
3. **Press Microphone** - Speak your query naturally
4. **Get Results** - View relevant schemes/programs with details
5. **Explore** - Tap "Show More Details" on any card

### Voice Commands Examples

**English:**
- "I am a farmer, what schemes are available?"
- "Show me scholarships for students"
- "What are the government jobs for graduates?"
- "Where can I sell vegetables?"

**Hindi:**
- "मैं एक किसान हूं, कौन सी योजनाएं उपलब्ध हैं?"
- "छात्रों के लिए छात्रवृत्ति दिखाएं"
- "स्नातकों के लिए सरकारी नौकरियां क्या हैं?"
- "मैं सब्जियां कहां बेच सकता हूं?"

## Project Structure

```
bharat-sahayak/
├── app/
│   ├── layout.tsx          # Root layout
│   ├── page.tsx            # Main page
│   └── globals.css         # Global styles
├── components/
│   ├── HomePage.tsx        # Landing page with categories
│   └── VoiceInterface.tsx  # Voice interaction & results
├── data/
│   ├── schemes.json        # Government schemes data
│   ├── education.json      # Scholarships & skill programs
│   ├── jobs.json           # Government job opportunities
│   └── markets.json        # Local market information
└── README.md
```

## Data Sources

All information is sourced from official government portals:
- Ministry of Agriculture & Farmers Welfare
- National Health Authority
- Ministry of Education
- Ministry of Skill Development
- Staff Selection Commission
- Railway Recruitment Board
- IBPS, UPSC, State PSCs

## Browser Compatibility

- **Best Experience**: Chrome, Edge (full voice support)
- **Limited Support**: Firefox, Safari (may have voice limitations)
- **Mobile**: Works on Android Chrome, iOS Safari

## Accessibility Features

- Large touch targets for easy interaction
- High contrast colors for readability
- Slow speech mode for elderly users
- Simple language explanations
- Visual feedback during voice interaction
- Repeat and explain-simply options

## Limitations (Demo Scope)

This is a prototype with controlled scope:
- No authentication or user accounts
- No real-time government API integration
- Static datasets (updated manually)
- No form submission or application processing
- No payment processing
- No persistent data storage

## Future Enhancements

- Real-time government API integration
- Location-based services (GPS)
- Regional language support (Tamil, Telugu, Bengali, etc.)
- Offline mode with cached data
- SMS/WhatsApp integration
- Application tracking
- Document upload assistance

## Contributing

This is a demo project. For production use, integrate with official government APIs and add proper authentication.

## License

Educational/Demo Project - Not for commercial use

---

Built with ❤️ for Bharat
