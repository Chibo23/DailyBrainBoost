# Daily Brain Boost - App Redesign Prompt

## Overview
Redesign the Daily Brain Boost application into a multi-page, dynamic trivia platform with AI-generated questions, enhanced visuals, improved user engagement, and personalized difficulty levels.

---

## Page Structure

### 1. **Introduction/Landing Page**
- **Header**: Display app name "Daily Brain Boost" with a tagline "Test Your Mind"
- **Animated Brain Icon**: Create a simple, smooth animated brain icon (pulsing or rotating animation)
- **Call-to-Action**: Single "Start" button to navigate to the Topics page
- **Layout**: Centered, clean design with ample whitespace
- **Visual Feature**: Add an animated illustration of a person thinking with a lightbulb or idea cloud above their head (right/left side of the page)
- **Brain Facts Animation**: Animated thought bubble or cloud display beside/above the person showing rotating brain facts (changes every 3-4 seconds)

---

### 2. **Topics Selection Page**
- **Header**: "Select Your Challenge" or "Choose Your Topic"
- **Topic Cards**: Display all available topics with:
  - **Icon for each topic** (SVG or emoji icons):
    - 🧬 Computer Science
    - 🏥 Medicine
    - 💼 Business
    - 🧩 General Logic
  - Topic name
  - Brief description (optional)
  - Interactive hover effects (scale, glow, color change)
- **Layout**: Grid layout (2x2 or responsive) with equal-sized cards
- **Navigation**: Back button to return to intro page

---

### 3. **Difficulty Selection Page**
- **Header**: "Select Difficulty Level" with the chosen topic displayed
- **Difficulty Options**:
  - Easy (Beginner)
  - Medium (Intermediate)
  - Hard (Advanced)
  - Expert (Master)
- **Each option displays**:
  - Difficulty name and icon/badge
  - Brief description (e.g., "Perfect for beginners")
  - Color-coded styling
- **Navigation**: "Back" button to return to topics page
- **Visual Feedback**: Show selected difficulty with prominent styling

---

### 4. **Quiz/Trivia Page**
- **Header Section**:
  - Topic name and difficulty level
  - Progress bar showing current question (e.g., "Question 3 of 10")
  - Score/Points counter (correct answers out of total)
  
- **Main Content Area**:
  - **Current Question**: Displayed prominently and clearly
  - **Answer Input Field**: Text input for user to type their answer
  - **Feedback Area**: Shows "Correct ✅" or "Wrong ❌" with the correct answer displayed after submission
  
- **Buttons**:
  - **Submit Button**: Submit the current answer
  - **Next Button**: Proceed to the next question (shows after answer submission)
  - **Quit Button**: Exit the trivia with confirmation dialog (e.g., "Are you sure you want to quit? Your progress will not be saved.")
  - **Enter Key Support**: Allow pressing Enter to submit answers
  
- **Brain Facts Display** (Side Panel or Bottom Section):
  - Animated illustration of a person with a thought bubble above
  - Rotating brain facts displayed in the thought bubble (auto-changes every 4 seconds)
  - Facts should be visually distinct and easy to read
  - All facts must be exclusively about the brain

- **Design Elements**:
  - Modern, engaging theme with smooth animations
  - Clear visual hierarchy
  - Responsive layout for different screen sizes
  - Smooth transitions between questions
  - Difficulty-appropriate color scheme (e.g., cool tones for easy, warm tones for hard)

---

### 5. **Results/Summary Page** (Optional)
- **Final Score**: "You scored X/10" or similar
- **Performance Breakdown**: 
  - Correct answers count
  - Wrong answers count
  - Accuracy percentage
- **Buttons**:
  - "Try Again" (same topic/difficulty)
  - "Change Topic" (back to topics page)
  - "Back to Home" (intro page)
- **Encouraging Message**: Based on performance (e.g., "Great job!" or "Keep practicing!")

---

## AI Integration Requirements

- **Dynamic Question Generation**: Questions should be AI-generated (using an AI API like OpenAI, Gemini, or similar)
- **No Hardcoded Questions**: Remove the static questions array
- **Randomization**: Each user gets different questions; two users will never get the same question set
- **Difficulty Scaling**: AI generates questions appropriate to the selected difficulty level
- **Question Variety**: Questions should vary by type (multiple-choice, short-answer, true/false, etc.)
- **Caching**: Consider caching questions to avoid API rate limits and improve performance

---

## Theme & Styling Updates

- **Color Scheme**: 
  - Primary: Modern gradient (consider deep purples, teals, or electric blues)
  - Secondary: Complementary accent colors
  - Difficulty-specific colors (Easy: soft green, Medium: warm orange, Hard: bold red, Expert: deep purple)
  
- **Typography**:
  - Modern, readable fonts (e.g., Inter, Poppins, or similar)
  - Clear hierarchy: Large headers, readable body text
  
- **Animations**:
  - Smooth page transitions
  - Button hover and click animations
  - Loading states for AI question fetching
  - Brain facts transition animations (fade in/out or slide)
  - Thought bubble animation for the illustrated person
  - Animated brain icon on intro page (pulsing, rotating, or morphing)
  
- **Visual Design**:
  - Modern, clean aesthetic
  - Card-based layouts where appropriate
  - Glassmorphism or neumorphism effects (optional)
  - Custom SVG icons for each topic
  - Illustrated character with animated thought bubble

---

## User Experience Enhancements

1. **Progress Tracking**: 
   - Visual progress bar showing current question number
   - Session statistics (correct/incorrect counts)

2. **Difficulty Selection**: 
   - Users can choose difficulty before starting
   - Difficulty affects question complexity and scoring

3. **Quit Functionality**: 
   - Mid-quiz quit button with confirmation
   - Clear messaging about progress loss

4. **Brain Facts**:
   - Only display facts about the brain (neuroscience, cognitive science, etc.)
   - Auto-rotate every 3-4 seconds
   - Animated presentation with the illustrated person

5. **Responsive Design**: 
   - Mobile-first approach
   - Works seamlessly on all device sizes
   - Touch-friendly buttons and inputs

---

## Technical Stack Recommendations

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Animations**: CSS animations, or Framer Motion/Anime.js
- **AI Integration**: OpenAI API, Google Gemini API, or similar
- **Backend**: Node.js, Python Flask, or serverless functions (AWS Lambda, Vercel Functions)
- **Database**: Optional (for storing user progress, stats)

---

## Brain Facts Database

All brain facts should focus exclusively on:
- Neurobiology and brain structure
- Cognitive science and memory
- Brain health and neuroplasticity
- Interesting brain phenomena
- Mental health and brain wellness
- Example: "Your brain generates 23 watts of power", "The brain has about 86 billion neurons"

---

## File Structure Suggestion

```
DailyBrainBoost/
├── index.html (Landing page)
├── topics.html (Topic selection)
├── difficulty.html (Difficulty selection)
├── quiz.html (Main quiz page)
├── results.html (Results page)
├── css/
│   ├── styles.css (Global styles)
│   ├── animations.css (Animation definitions)
│   └── responsive.css (Media queries)
├── js/
│   ├── app.js (Main app logic)
│   ├── ai-service.js (AI integration)
│   ├── brain-facts.js (Brain facts data)
│   └── utils.js (Utility functions)
├── assets/
│   ├── icons/ (Topic icons, difficulty badges)
│   ├── illustrations/ (Person with thought bubble)
│   └── animations/ (SVG animations)
└── config.js (API keys, settings)
```

---

## Additional Notes

- Maintain consistent branding throughout all pages
- Ensure accessibility (ARIA labels, keyboard navigation, color contrast)
- Implement error handling for AI API failures with fallback options
- Add loading spinners while fetching AI-generated questions
- Consider adding a statistics page for tracking user progress over time
- Implement smooth page transitions with animations
- Test on multiple devices and screen sizes
