# Bharat Sahayak - Design Document

## 1. Design Philosophy

### 1.1 Core Principles

**Voice-First, Mobile-First**
- Primary interaction through voice, not typing
- Optimized for mobile screens and touch interaction
- Large, accessible touch targets

**Simplicity for Low Digital Literacy**
- Minimal text, maximum clarity
- Large buttons with clear icons
- One primary action per screen
- Progressive disclosure of information

**Trust & Accessibility**
- Government service aesthetic (professional, trustworthy)
- High contrast colors for readability
- Calm, friendly tone
- Clear source attribution

**Inclusive Design**
- Bilingual support (Hindi + English)
- Slow speech mode for elderly
- Simple explanations available
- Family-friendly (parents can help children)

---

## 2. Visual Design System

### 2.1 Color Palette

**Primary Colors (India-inspired)**
- India Blue: `#000080` - Primary actions, headers
- India Orange: `#FF9933` - Accents, highlights
- India Green: `#138808` - Success states, positive actions

**Neutral Colors**
- White: `#FFFFFF` - Backgrounds, cards
- Gray 50: `#F9FAFB` - Subtle backgrounds
- Gray 100: `#F3F4F6` - Borders
- Gray 600: `#4B5563` - Secondary text
- Gray 700: `#374151` - Body text
- Gray 800: `#1F2937` - Headings

**Semantic Colors**
- Success: Green `#10B981`
- Error: Red `#EF4444`
- Warning: Yellow `#F59E0B`
- Info: Blue `#3B82F6`

**Gradients**
- Background: Orange-50 to Green-50 (subtle, calming)

### 2.2 Typography

**Font Family**
- System fonts for performance and familiarity
- `-apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto'`
- Supports Devanagari (Hindi) script

**Font Sizes**
- Heading 1: 48-60px (App title)
- Heading 2: 36px (Category titles)
- Heading 3: 24px (Card titles)
- Body Large: 20px (Instructions)
- Body: 16-18px (Content)
- Small: 14px (Metadata)

**Font Weights**
- Bold (700): Headings, buttons
- Semibold (600): Subheadings
- Regular (400): Body text

### 2.3 Spacing System

**Base Unit**: 4px

**Scale**
- xs: 4px
- sm: 8px
- md: 16px
- lg: 24px
- xl: 32px
- 2xl: 48px
- 3xl: 64px

### 2.4 Border Radius
- Small: 8px (buttons)
- Medium: 12px (cards)
- Large: 16px (modals)
- XL: 24px (hero elements)
- Full: 9999px (circular buttons)

### 2.5 Shadows
- Small: `0 1px 2px rgba(0,0,0,0.05)`
- Medium: `0 4px 6px rgba(0,0,0,0.1)`
- Large: `0 10px 15px rgba(0,0,0,0.1)`
- XL: `0 20px 25px rgba(0,0,0,0.15)`

---

## 3. Component Design

### 3.1 Home Screen

**Layout**
```
┌─────────────────────────────┐
│                             │
│      Bharat Sahayak         │
│   Speak. Discover. Access.  │
│                             │
│   [English]  [हिंदी]        │
│                             │
│  ┌──────┐    ┌──────┐       │
│  │  🏛️  │    │  📚  │       │
│  │Public│    │ Edu  │       │
│  └──────┘    └──────┘       │
│                             │
│  ┌──────┐    ┌──────┐       │
│  │  💼  │    │  🏪  │       │
│  │ Jobs │    │Market│       │
│  └──────┘    └──────┘       │
│                             │
│  Tap any category to start  │
└─────────────────────────────┘
```

**Elements**
- App title: 60px, bold, India Blue
- Tagline: 24px, gray-700
- Language toggle: 2 buttons, rounded-full
- Category grid: 2x2, large cards with icons
- Instruction text: 20px, gray-600

**Interactions**
- Language buttons: Toggle active state
- Category cards: Scale on hover (1.05x), tap (0.95x)
- Smooth fade-in animations on load

### 3.2 Voice Interface Screen

**Layout**
```
┌─────────────────────────────┐
│ ← Back      [EN] [HI]       │
│                             │
│    Public Services          │
│  Press microphone & speak   │
│                             │
│         ┌─────┐             │
│         │ 🎤  │             │
│         └─────┘             │
│                             │
│    [Slow]  [Normal]         │
│                             │
│  ┌─────────────────────┐    │
│  │ You said: ...       │    │
│  └─────────────────────┘    │
│                             │
│  ┌─────────────────────┐    │
│  │ AI Response         │    │
│  │ [Repeat] [Explain]  │    │
│  └─────────────────────┘    │
│                             │
│  ┌─────────────────────┐    │
│  │ Result Card 1       │    │
│  └─────────────────────┘    │
└─────────────────────────────┘
```

**Microphone Button**
- Size: 128x128px
- Circular, centered
- States:
  - Idle: India Blue background, 🎤 icon
  - Listening: Red background, 🎙️ icon, pulse animation
  - Speaking: Green background, 🔊 icon

**Transcript Box**
- White background
- Rounded corners (16px)
- Shadow: medium
- Label: "You said:" (gray-500)
- Text: 20px, gray-800

**Response Box**
- India Blue background
- White text
- Rounded corners (16px)
- Shadow: large
- Action buttons: White bg, blue text

**Result Cards**
- White background
- Border: 2px gray-100
- Rounded: 16px
- Shadow: large
- Expandable sections

### 3.3 Result Card Design

**Collapsed State**
```
┌─────────────────────────────┐
│ PM-KISAN                    │
│ प्रधानमंत्री किसान सम्मान   │
│                             │
│ ₹6,000 per year in 3        │
│ installments                │
│                             │
│ 📋 Required Documents:      │
│ • Aadhaar Card              │
│ • Bank Account              │
│ • Land Records              │
│                             │
│ [Show More Details ▼]       │
└─────────────────────────────┘
```

**Expanded State**
```
┌─────────────────────────────┐
│ PM-KISAN                    │
│ प्रधानमंत्री किसान सम्मान   │
│                             │
│ ₹6,000 per year in 3        │
│ installments                │
│                             │
│ 📋 Required Documents:      │
│ • Aadhaar Card              │
│ • Bank Account              │
│ • Land Records              │
│                             │
│ ✅ How to Apply:            │
│ 1. Visit PM-KISAN portal    │
│ 2. Fill registration form   │
│ 3. Upload documents         │
│ 4. Submit & get ack         │
│                             │
│ 🔗 Source: Ministry of      │
│    Agriculture              │
│                             │
│ [Show Less ▲]               │
└─────────────────────────────┘
```

**Card Elements**
- Title: 24px, bold, India Blue
- Hindi title: 18px, gray-600
- Benefit: 18px, gray-700
- Icons: 20px, inline with labels
- Lists: Bullet/numbered, 16px
- Expand button: Full width, India Blue bg

---

## 4. Interaction Design

### 4.1 Voice Interaction Flow

**Step 1: Category Selection**
- User taps category card
- Smooth transition to voice interface
- Category name displayed at top

**Step 2: Voice Input**
- User presses microphone button
- Button turns red with pulse animation
- Browser requests microphone permission (first time)
- Recording starts immediately

**Step 3: Speech Recognition**
- User speaks naturally
- System converts speech to text
- Transcript displayed in box
- Button returns to idle state

**Step 4: Query Processing**
- System analyzes transcript
- Matches keywords to database
- Generates response text
- Displays results

**Step 5: Voice Output**
- System speaks response using TTS
- Microphone button shows green (speaking state)
- User can see and hear response simultaneously

**Step 6: Result Exploration**
- Result cards appear with animation
- User can tap to expand details
- User can use Repeat/Explain buttons
- User can start new query

### 4.2 Animation Specifications

**Page Transitions**
- Duration: 300ms
- Easing: ease-in-out
- Fade + slide (20px)

**Card Animations**
- Stagger: 100ms between cards
- Fade in + scale (0.95 → 1)
- Duration: 200ms

**Button Interactions**
- Hover: Scale 1.05, duration 150ms
- Tap: Scale 0.95, duration 100ms
- Active state: Immediate color change

**Microphone Pulse**
- Scale: 1 → 1.1 → 1
- Duration: 1000ms
- Infinite loop while listening

**Expand/Collapse**
- Height: auto animation
- Duration: 300ms
- Easing: ease-in-out

### 4.3 Error Handling

**Voice Recognition Error**
- Display message: "Sorry, I could not hear you clearly"
- Hindi: "क्षमा करें, मैं आपको स्पष्ट रूप से नहीं सुन सका"
- Show retry button
- Microphone returns to idle state

**No Results Found**
- Display: "I couldn't find exact matches, but here are some options"
- Show 2-3 general results
- Encourage user to try different words

**Browser Not Supported**
- Alert: "Voice recognition not supported"
- Suggest Chrome or Edge
- Provide fallback text input (future)

---

## 5. Responsive Design

### 5.1 Breakpoints

- Mobile: 320px - 767px
- Tablet: 768px - 1023px
- Desktop: 1024px+

### 5.2 Mobile (Primary Target)

**Home Screen**
- Single column layout
- Category grid: 2x2
- Full-width cards
- Padding: 24px

**Voice Interface**
- Full-width elements
- Microphone: 96px (smaller)
- Cards: Full width with 16px margin

### 5.3 Tablet

**Home Screen**
- Category grid: 2x2 (larger cards)
- Max-width: 600px, centered
- Padding: 32px

**Voice Interface**
- Max-width: 768px, centered
- Microphone: 128px
- Cards: Full width

### 5.4 Desktop

**Home Screen**
- Max-width: 800px, centered
- Category grid: 2x2 (largest cards)
- Padding: 48px

**Voice Interface**
- Max-width: 1024px, centered
- Two-column layout for results (optional)
- Larger spacing

---

## 6. Accessibility Design

### 6.1 Visual Accessibility

**Color Contrast**
- Text on white: Minimum 4.5:1 ratio
- White on India Blue: 7:1 ratio
- All text meets WCAG AA standards

**Focus States**
- Visible outline: 2px solid India Blue
- Offset: 2px
- All interactive elements have focus states

**Text Sizing**
- Minimum 16px for body text
- Scalable with browser zoom
- No fixed pixel heights

### 6.2 Motor Accessibility

**Touch Targets**
- Minimum: 48x48px
- Spacing: 8px between targets
- Large buttons for primary actions

**Timing**
- No time limits on interactions
- User controls speech rate
- Can replay responses unlimited times

### 6.3 Cognitive Accessibility

**Simple Language**
- Short sentences
- Common words
- Active voice
- Clear instructions

**Visual Hierarchy**
- One primary action per screen
- Clear headings
- Consistent layout
- Predictable navigation

**Error Prevention**
- Confirmation for destructive actions
- Clear error messages
- Easy recovery

### 6.4 Auditory Accessibility

**Visual Feedback**
- Transcript shown for all voice input
- Visual indicators during speech
- Text alternative for all audio

**Speech Control**
- Adjustable speech rate
- Pause/replay options
- Volume controlled by device

---

## 7. Content Design

### 7.1 Tone & Voice

**Characteristics**
- Friendly but professional
- Helpful, not patronizing
- Clear and direct
- Culturally appropriate

**Examples**
- Good: "I found 3 schemes that can help you"
- Bad: "Here are your search results"

- Good: "Let me explain this simply"
- Bad: "Click here for more information"

### 7.2 Bilingual Content Strategy

**Language Switching**
- Instant switch without page reload
- All content available in both languages
- Consistent terminology

**Hindi Content**
- Devanagari script
- Formal but accessible Hindi
- Common terms, not overly Sanskritized
- Technical terms in English when appropriate

**English Content**
- Indian English conventions
- Simple vocabulary
- Short sentences
- Active voice

### 7.3 Microcopy

**Buttons**
- English: "Show More Details", "Repeat", "Explain Simply"
- Hindi: "अधिक विवरण दिखाएं", "दोहराएं", "सरल समझाएं"

**Instructions**
- English: "Press the microphone and speak"
- Hindi: "माइक्रोफ़ोन दबाएं और बोलें"

**Feedback**
- English: "Listening...", "Speaking..."
- Hindi: "सुन रहा हूं...", "बोल रहा हूं..."

---

## 8. Data Presentation Design

### 8.1 Government Schemes

**Card Structure**
1. Scheme name (bilingual)
2. Benefit summary (1-2 lines)
3. Required documents (bulleted list)
4. Application steps (numbered list)
5. Official source

**Visual Hierarchy**
- Name: Largest, bold, blue
- Benefit: Medium, gray
- Documents: Small, with icon
- Steps: Numbered, expandable
- Source: Smallest, gray

### 8.2 Education Programs

**Card Structure**
1. Program name (bilingual)
2. Type badge (scholarship/skill)
3. Amount/benefit
4. Eligibility summary
5. Application process
6. Official source

**Visual Elements**
- Amount: Green color, prominent
- Type badge: Small pill, colored
- Courses: Grid or list with icons

### 8.3 Government Jobs

**Card Structure**
1. Job/exam name (bilingual)
2. Department
3. Positions available
4. Salary range (green, prominent)
5. Eligibility (age, education)
6. Exam pattern
7. Application process
8. Frequency

**Visual Hierarchy**
- Job name: Largest, bold
- Salary: Green, second most prominent
- Eligibility: Boxed section
- Details: Expandable

### 8.4 Local Markets

**Card Structure**
1. Market name (bilingual)
2. Location (state/district)
3. Products accepted
4. Timings
5. Contact information

**Visual Elements**
- Location: With 📍 icon
- Timings: With 🕐 icon
- Contact: With 📞 icon, clickable

---

## 9. Technical Design Considerations

### 9.1 Performance Optimization

**Image Optimization**
- Use emoji instead of images for icons
- No heavy graphics
- SVG for any custom icons

**Code Splitting**
- Lazy load components
- Split by route
- Minimize bundle size

**Caching**
- Cache JSON data
- Service worker for offline (future)
- Browser caching headers

### 9.2 Progressive Enhancement

**Core Functionality**
- Works without JavaScript (basic content)
- Voice features require JavaScript
- Graceful degradation

**Browser Support**
- Modern browsers: Full experience
- Older browsers: Basic content access
- Clear messaging about requirements

---

## 10. Design Tokens

### 10.1 Tailwind Configuration

```javascript
colors: {
  'india-orange': '#FF9933',
  'india-green': '#138808',
  'india-blue': '#000080',
}

fontSize: {
  'xs': '12px',
  'sm': '14px',
  'base': '16px',
  'lg': '18px',
  'xl': '20px',
  '2xl': '24px',
  '3xl': '30px',
  '4xl': '36px',
  '5xl': '48px',
  '6xl': '60px',
}

spacing: {
  '1': '4px',
  '2': '8px',
  '3': '12px',
  '4': '16px',
  '6': '24px',
  '8': '32px',
  '12': '48px',
  '16': '64px',
}
```

---

**Document Version**: 1.0  
**Last Updated**: February 2026  
**Status**: Approved for Development
