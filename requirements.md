# Bharat Sahayak - Requirements Document

## Project Overview

**Project Name**: Bharat Sahayak (भारत सहायक)  
**Tagline**: Speak. Discover. Access.  
**Purpose**: A voice-first, multilingual AI assistant helping Indian citizens access public services, government schemes, education programs, government jobs, and local community resources.

---

## Target Audience

### Primary Users
- Indian citizens with low to moderate digital literacy
- Rural and semi-urban populations
- Students and youth seeking education/job opportunities
- Farmers and small business owners
- Elderly citizens needing government services
- Families seeking welfare schemes

### User Characteristics
- Age range: 15-65+ years
- Digital literacy: Low to moderate
- Language preference: Hindi and English (with potential for regional languages)
- Device access: Primarily mobile phones
- Internet: May have limited or intermittent connectivity

---

## Functional Requirements

### 1. Core Features

#### 1.1 Voice Interaction
- **FR-1.1.1**: System shall support speech-to-text conversion in Hindi and English
- **FR-1.1.2**: System shall support text-to-speech output in Hindi and English
- **FR-1.1.3**: Users shall be able to press a microphone button to start voice input
- **FR-1.1.4**: System shall display transcript of user's spoken query
- **FR-1.1.5**: System shall provide adjustable speech rate (slow/normal)
- **FR-1.1.6**: System shall provide "Repeat" functionality to replay AI response
- **FR-1.1.7**: System shall provide "Explain Simply" option for simplified explanations

#### 1.2 Language Support
- **FR-1.2.1**: System shall support English and Hindi languages
- **FR-1.2.2**: Users shall be able to switch languages at any time
- **FR-1.2.3**: All content (schemes, jobs, education) shall be available in both languages
- **FR-1.2.4**: Voice recognition shall work in both Hindi and English

#### 1.3 Category Navigation
- **FR-1.3.1**: System shall provide four main categories:
  - Public Services & Government Schemes
  - Education & Skill Development
  - Government Job Opportunities
  - Local Markets & Community Resources
- **FR-1.3.2**: Each category shall have a distinct icon and clear label
- **FR-1.3.3**: Users shall be able to navigate back to home screen from any category

### 2. Public Services & Government Schemes

#### 2.1 Scheme Discovery
- **FR-2.1.1**: System shall provide information on major government schemes including:
  - PM-KISAN (farmer income support)
  - Ayushman Bharat (health insurance)
  - Pradhan Mantri Ujjwala Yojana (LPG connection)
  - Pradhan Mantri Awas Yojana (housing)
- **FR-2.1.2**: System shall match user queries to relevant schemes based on keywords
- **FR-2.1.3**: System shall display scheme eligibility criteria
- **FR-2.1.4**: System shall show required documents for each scheme
- **FR-2.1.5**: System shall provide step-by-step application guidance
- **FR-2.1.6**: System shall cite official government sources

#### 2.2 Eligibility Detection
- **FR-2.2.1**: System shall ask conversational questions to determine eligibility:
  - Age range
  - State/location
  - Occupation
  - Income range (optional)
  - Land ownership (for agricultural schemes)
- **FR-2.2.2**: System shall explain why user is eligible for specific schemes
- **FR-2.2.3**: System shall use simple, non-official language

### 3. Education & Skill Development

#### 3.1 Scholarship Discovery
- **FR-3.1.1**: System shall provide information on scholarships including:
  - National Scholarship Portal schemes
  - Begum Hazrat Mahal Scholarship
  - State-specific scholarships
- **FR-3.1.2**: System shall show scholarship amounts and eligibility
- **FR-3.1.3**: System shall display application process and deadlines

#### 3.2 Skill Development Programs
- **FR-3.2.1**: System shall provide information on skill programs including:
  - Pradhan Mantri Kaushal Vikas Yojana (PMKVY)
  - DDU-GKY (rural youth training)
- **FR-3.2.2**: System shall list available courses/trades
- **FR-3.2.3**: System shall show training centers and enrollment process
- **FR-3.2.4**: System shall explain monetary rewards and placement support

### 4. Government Job Opportunities

#### 4.1 Job Discovery
- **FR-4.1.1**: System shall provide information on government jobs including:
  - SSC (Staff Selection Commission) exams
  - Railway Recruitment Board exams
  - Banking exams (IBPS)
  - UPSC Civil Services
  - State PSC exams
  - Teaching jobs (CTET)
- **FR-4.1.2**: System shall match jobs based on user's education level
- **FR-4.1.3**: System shall display salary ranges
- **FR-4.1.4**: System shall show eligibility criteria (age, education)
- **FR-4.1.5**: System shall explain exam pattern and application process
- **FR-4.1.6**: System shall indicate exam frequency

### 5. Local Markets & Community Resources

#### 5.1 Market Information
- **FR-5.1.1**: System shall provide information on wholesale markets
- **FR-5.1.2**: System shall show market location (state/district)
- **FR-5.1.3**: System shall display market timings
- **FR-5.1.4**: System shall provide contact information
- **FR-5.1.5**: System shall list products accepted at each market

---

## Non-Functional Requirements

### 6. Usability

#### 6.1 Accessibility
- **NFR-6.1.1**: Interface shall use high-contrast colors for readability
- **NFR-6.1.2**: Touch targets shall be minimum 48x48 pixels
- **NFR-6.1.3**: Text shall be minimum 16px for body, 24px for headings
- **NFR-6.1.4**: System shall work with screen readers
- **NFR-6.1.5**: System shall support slow speech mode for elderly users

#### 6.2 User Experience
- **NFR-6.2.1**: Home screen shall load within 2 seconds
- **NFR-6.2.2**: Voice recognition shall start within 1 second of button press
- **NFR-6.2.3**: System shall provide visual feedback during voice interaction
- **NFR-6.2.4**: Error messages shall be clear and actionable
- **NFR-6.2.5**: System shall use calm, friendly, trustworthy tone

### 7. Performance

#### 7.1 Response Time
- **NFR-7.1.1**: Voice-to-text conversion shall complete within 3 seconds
- **NFR-7.1.2**: Query processing shall complete within 2 seconds
- **NFR-7.1.3**: Text-to-speech shall start within 1 second
- **NFR-7.1.4**: Page transitions shall be smooth (60fps)

#### 7.2 Scalability
- **NFR-7.2.1**: System shall support up to 100 concurrent users (demo scope)
- **NFR-7.2.2**: Dataset shall be easily expandable with new schemes/jobs

### 8. Compatibility

#### 8.1 Browser Support
- **NFR-8.1.1**: System shall work on Chrome 90+
- **NFR-8.1.2**: System shall work on Edge 90+
- **NFR-8.1.3**: System shall provide graceful degradation on Firefox/Safari
- **NFR-8.1.4**: Voice features shall work on Android Chrome
- **NFR-8.1.5**: Voice features shall work on iOS Safari (with limitations)

#### 8.2 Device Support
- **NFR-8.2.1**: System shall be responsive on mobile devices (320px+)
- **NFR-8.2.2**: System shall work on tablets and desktops
- **NFR-8.2.3**: System shall be touch-optimized

### 9. Security & Privacy

#### 9.1 Data Privacy
- **NFR-9.1.1**: System shall not store user voice recordings
- **NFR-9.1.2**: System shall not collect personal information
- **NFR-9.1.3**: System shall not require user authentication (demo scope)
- **NFR-9.1.4**: System shall process voice locally in browser

### 10. Reliability

#### 10.1 Error Handling
- **NFR-10.1.1**: System shall handle voice recognition failures gracefully
- **NFR-10.1.2**: System shall provide clear error messages in user's language
- **NFR-10.1.3**: System shall allow users to retry failed operations
- **NFR-10.1.4**: System shall work offline with cached data (future enhancement)

---

## Technical Requirements

### 11. Technology Stack

#### 11.1 Frontend
- **TR-11.1.1**: Framework: Next.js 14+ with React 18+
- **TR-11.1.2**: Language: TypeScript
- **TR-11.1.3**: Styling: Tailwind CSS
- **TR-11.1.4**: Animations: Framer Motion
- **TR-11.1.5**: Voice: Web Speech API (SpeechRecognition & SpeechSynthesis)

#### 11.2 Data Management
- **TR-11.2.1**: Data format: JSON files
- **TR-11.2.2**: Data structure: Bilingual (English + Hindi)
- **TR-11.2.3**: Data categories: schemes, education, jobs, markets

### 12. Data Requirements

#### 12.1 Government Schemes Dataset
- **DR-12.1.1**: Minimum 4 major schemes
- **DR-12.1.2**: Each scheme shall include:
  - Name (English + Hindi)
  - Category
  - Benefit description
  - Eligibility criteria
  - Required documents
  - Application steps
  - Official source

#### 12.2 Education Dataset
- **DR-12.2.1**: Minimum 4 programs (scholarships + skill training)
- **DR-12.2.2**: Each program shall include:
  - Name (English + Hindi)
  - Type (scholarship/skill)
  - Benefit/amount
  - Eligibility
  - Documents required
  - Application process
  - Official source

#### 12.3 Jobs Dataset
- **DR-12.3.1**: Minimum 6 government job categories
- **DR-12.3.2**: Each job shall include:
  - Name (English + Hindi)
  - Department
  - Positions
  - Salary range
  - Eligibility (education, age)
  - Exam pattern
  - Application process
  - Frequency

#### 12.4 Markets Dataset
- **DR-12.4.1**: Minimum 2 wholesale markets
- **DR-12.4.2**: Each market shall include:
  - Name (English + Hindi)
  - State/location
  - Type (wholesale/retail)
  - Products accepted
  - Timings
  - Contact information

---

## Scope Constraints (Demo Version)

### 13. Out of Scope

The following features are explicitly OUT OF SCOPE for the demo prototype:

- **OOS-13.1**: User authentication and login system
- **OOS-13.2**: User profile creation and management
- **OOS-13.3**: Real-time government API integration
- **OOS-13.4**: Form submission to government portals
- **OOS-13.5**: Payment processing
- **OOS-13.6**: Document upload functionality
- **OOS-13.7**: Application tracking system
- **OOS-13.8**: SMS/Email notifications
- **OOS-13.9**: Admin dashboard
- **OOS-13.10**: Database integration
- **OOS-13.11**: Persistent user data storage
- **OOS-13.12**: GPS-based location services
- **OOS-13.13**: Multi-user accounts
- **OOS-13.14**: Chat history persistence

---

## Success Criteria

### 14. Acceptance Criteria

The project shall be considered successful when:

- **AC-14.1**: Users can successfully interact using voice in Hindi and English
- **AC-14.2**: All four categories are functional and accessible
- **AC-14.3**: Voice recognition accuracy is above 80% in quiet environments
- **AC-14.4**: All scheme/job/education information is accurate and sourced
- **AC-14.5**: Application runs smoothly on mobile devices
- **AC-14.6**: Users can complete a full interaction flow (speak → get results → view details)
- **AC-14.7**: Interface is intuitive for users with low digital literacy
- **AC-14.8**: All content is available in both languages
- **AC-14.9**: Application loads and responds within specified time limits
- **AC-14.10**: Demo can be presented without internet (using cached data)

---

## Future Enhancements (Post-Demo)

### 15. Planned Features

- **FE-15.1**: Integration with real government APIs
- **FE-15.2**: Support for regional languages (Tamil, Telugu, Bengali, Marathi, etc.)
- **FE-15.3**: GPS-based location services for nearby centers
- **FE-15.4**: Document upload and verification
- **FE-15.5**: Application status tracking
- **FE-15.6**: SMS/WhatsApp integration for notifications
- **FE-15.7**: Offline mode with progressive web app (PWA)
- **FE-15.8**: Video tutorials for complex processes
- **FE-15.9**: Community forum for peer support
- **FE-15.10**: AI-powered personalized recommendations
- **FE-15.11**: Integration with DigiLocker for documents
- **FE-15.12**: Aadhaar-based authentication

---

## Compliance & Standards

### 16. Government Guidelines

- **CG-16.1**: All information shall be sourced from official government portals
- **CG-16.2**: Application shall follow Web Content Accessibility Guidelines (WCAG) 2.1 Level AA
- **CG-16.3**: Application shall comply with IT Act 2000 and amendments
- **CG-16.4**: Application shall follow Digital India accessibility guidelines
- **CG-16.5**: All government scheme information shall include official source attribution

---

## Glossary

- **Voice-First**: Interface designed primarily for voice interaction
- **Low Digital Literacy**: Users with limited experience using digital devices
- **Web Speech API**: Browser API for speech recognition and synthesis
- **CSC**: Common Service Center
- **SECC**: Socio-Economic Caste Census
- **BPL**: Below Poverty Line
- **NSP**: National Scholarship Portal
- **PMKVY**: Pradhan Mantri Kaushal Vikas Yojana
- **SSC**: Staff Selection Commission
- **UPSC**: Union Public Service Commission
- **IBPS**: Institute of Banking Personnel Selection

---

**Document Version**: 1.0  
**Last Updated**: February 2026  
**Status**: Approved for Demo Development
