# SHLOKA (श्लोक) - Bhagavad Gita Guidance by Emotion

## 📱 Overview
SHLOKA is a mobile application that makes the Bhagavad Gita accessible through **emotions**, not chapters. Designed for older adults (50-75+) who seek spiritual guidance in simple, calming language.

## ✨ Key Features

### 1. **Emotion-First Navigation**
Instead of asking "Which chapter?", SHLOKA asks:
> **"What is troubling you today?"**

Choose from 5 core emotions:
- 😟 **Fear (भय)** - Anxiety, worry, death
- 😠 **Anger (क्रोध)** - Frustration, injustice, rage
- 😢 **Grief (शोक)** - Loss, sadness, mourning
- 😕 **Confusion (मोह)** - Uncertainty, purpose, meaning
- 😶 **Detachment (वैराग्य)** - Loneliness, emptiness, disconnection

### 2. **Mood Refinement**
Each emotion has 3-4 specific moods to help pinpoint your exact feeling.

### 3. **Authentic Bhagavad Gita Guidance**
Each mood provides:
- 📖 **Sanskrit Verse** - Original shloka from Bhagavad Gita
- 🔤 **English Translation** - Clear, accurate translation
- 💡 **Contextual Guidance** - How this teaching applies to your situation

### 4. **Offline-First**
- Content cached locally after first load
- Works without internet connection
- Perfect for meditation or quiet reflection

### 5. **Personal Bookmarks**
- Save guidance that resonates with you
- Access anytime from Bookmarks screen
- Stored locally on your device

## 🎨 Design Philosophy

### For Older Adults
- **Large text** (18-28px) for easy reading
- **High contrast colors** for visibility
- **Large touch targets** (minimum 60px) for easy tapping
- **Simple navigation** with clear back buttons
- **No clutter** - calm, focused interface

### Color Palette
- 🟤 **Warm Cream** (#FAF7F2) - Main background
- 🟡 **Soft Saffron** (#F4E4C1) - Headers and accents
- 🟫 **Earth Brown** (#8B7355) - Primary text and buttons
- 🔵 **Gentle Blue** (#6B9BD1) - Action buttons

## 🗂️ App Structure

```
Home Screen (index.tsx)
    ↓ Select Emotion
Moods Screen (moods.tsx)
    ↓ Select Mood
Guidance Screen (guidance.tsx)
    ↓ Bookmark (optional)
Bookmarks Screen (bookmarks.tsx)
```

## 📊 Sample Content Included

### Emotions: 5
- Fear, Anger, Grief, Confusion, Detachment

### Moods: 15
- 3 moods per emotion
- Examples: "Fear of Future", "Anger at Injustice", "Loss of a Loved One"

### Guidance: 6
Each with authentic Bhagavad Gita verses:
- BG 2.47 - Focus on duty, not results (Fear)
- BG 2.20 - The soul is eternal (Fear of death)
- BG 2.63 - Anger destroys wisdom (Anger)
- BG 2.27 - Nature's cycle (Grief)
- BG 18.66 - Surrender to divine will (Confusion)
- BG 9.29 - You are never alone (Detachment)

## 🔧 Technical Stack

### Frontend
- **Expo** - React Native framework
- **TypeScript** - Type safety
- **AsyncStorage** - Local caching and bookmarks
- **Expo Router** - File-based navigation

### Backend
- **FastAPI** - Python web framework
- **MongoDB** - Database with sample data
- **Motor** - Async MongoDB driver

### API Endpoints
```
GET /api/emotions          - List all emotions
GET /api/moods/{emotion_id} - Get moods for an emotion
GET /api/guidance/{mood_id} - Get guidance for a mood
```

## 📝 Content Management

### Current Sample Data
The app includes sample content to demonstrate functionality. You can:

1. **View MongoDB Data** directly to understand structure
2. **Replace Sample Content** with full Bhagavad Gita mapping
3. **Add More Emotions** or moods as needed
4. **Update Guidance** with different translations or commentaries

### Data Structure
```javascript
// Emotion
{
  _id: "fear",
  name_english: "Fear",
  name_sanskrit: "भय (Bhaya)",
  description: "When you feel afraid...",
  icon: "😰"
}

// Mood
{
  _id: "fear_future",
  emotion_id: "fear",
  name: "Fear of the Future",
  description: "Worried about what tomorrow will bring"
}

// Guidance
{
  _id: "guidance_fear_future",
  mood_id: "fear_future",
  title: "Focus on Your Duty, Not Results",
  verse_reference: "Bhagavad Gita 2.47",
  sanskrit_verse: "कर्मण्येवाधिकारस्ते...",
  english_translation: "You have the right...",
  guidance_text: "Krishna teaches that..."
}
```

## 🚀 Future Enhancements (Post-MVP)

### Content
- [ ] Complete all 700 verses of Bhagavad Gita
- [ ] Multiple translation options
- [ ] Commentary from different scholars
- [ ] More emotions and moods

### Features
- [ ] Audio playback (Text-to-Speech)
- [ ] Search functionality
- [ ] Daily wisdom notifications
- [ ] Share guidance with others
- [ ] Reading history
- [ ] Font size adjustments
- [ ] Dark mode

### Technical
- [ ] User accounts (optional)
- [ ] Cloud sync for bookmarks
- [ ] Analytics
- [ ] Multiple languages (Hindi, etc.)

## 🎯 User Journey

1. **Open App** → See calming interface with Sanskrit title
2. **Read Question** → "What is troubling you today?"
3. **Select Emotion** → Tap on what you feel (e.g., "Fear")
4. **Choose Mood** → Pick specific feeling (e.g., "Fear of Death")
5. **Read Guidance** → See Sanskrit verse + translation + guidance
6. **Bookmark** → Save for later if it helps
7. **Return Home** → Explore more or exit feeling calmer

## 🧘 Design Principles Followed

✅ **Emotion-first, not scripture-first**
✅ **Meaning over verses** (verses referenced, not dumped)
✅ **Calm, slow, dignified UX**
✅ **Offline-first**
✅ **No ads, no social feed, no gamification**
✅ **No reinterpretation** - authentic Gita teachings
✅ **Mobile-optimized** for touch interactions
✅ **Accessible** for older adults

## 📱 Testing the App

### On Expo Go App (Recommended)
1. Install Expo Go on your phone (iOS/Android)
2. Scan the QR code provided in the terminal
3. App loads on your device

### On Web Preview
- Access via the web URL provided
- Test basic functionality

### Test Flow
1. Select an emotion (e.g., "Fear")
2. Select a mood (e.g., "Fear of Death")
3. Read the guidance from Bhagavad Gita 2.20
4. Bookmark it
5. Go to Bookmarks screen to see saved guidance
6. Close and reopen app - data should be cached

## 📖 About Bhagavad Gita

The Bhagavad Gita is a 700-verse Hindu scripture that is part of the epic Mahabharata. It consists of a conversation between Prince Arjuna and the god Krishna, who serves as his charioteer. The Gita addresses the moral and philosophical dilemmas Arjuna faces and provides guidance on:

- **Dharma** (righteous duty)
- **Karma** (action and consequences)
- **Yoga** (spiritual practice)
- **Moksha** (liberation)

SHLOKA makes these timeless teachings accessible by organizing them around universal human emotions.

## 🙏 Credits

- **Design Philosophy**: Focused on dignity, simplicity, and accessibility
- **Content**: Authentic Bhagavad Gita verses with contextual guidance
- **Target Audience**: Older adults seeking spiritual clarity
- **Cultural Respect**: No distortion or reinterpretation of scripture

---

**Built with ❤️ for those seeking peace and wisdom**
