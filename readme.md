# Bible Quiz Game - Instructions

## 📖 Overview
A bilingual (English/Portuguese) Bible quiz game that works on both desktop and mobile devices. Features difficulty levels, Bible verse references, streak tracking, and comprehensive biblical explanations.

## 🎮 How to Use

### Desktop:
1. Simply double-click `bible-quiz-game.html` to open it in your browser
2. Or right-click → Open with → Your preferred browser

### Mobile:
1. Transfer the HTML file to your phone
2. Open it with any mobile browser (Chrome, Safari, Firefox, etc.)

## 🆕 New Features

### ✨ Bible Verse References
Every answer now includes:
- **The actual Bible verse** quoted directly from Scripture
- **Biblical reference** (e.g., Genesis 1:27, John 11:35)
- **Explanation** providing context and additional information

### 🎯 Difficulty Levels
- **Easy**: 10 questions - Perfect for beginners
- **Medium**: 15 questions - Good challenge for regular students
- **Hard**: 25 questions - Comprehensive test of Bible knowledge

### 🔥 Streak Counter
- Track consecutive correct answers
- See your best streak in the results screen
- Visual streak badge appears during gameplay

### 📊 Enhanced Statistics
Results now show:
- Score percentage
- Correct/Incorrect answer count
- Best streak achieved during the quiz

## ➕ How to Add More Questions

Open `bible-quiz-game.html` in any text editor and find the `questionsDatabase` section (around line 265). 

### NEW Format with Bible Verses:
```javascript
{
    question: "Your question here?",
    answers: ["Option 1", "Option 2", "Option 3", "Option 4"],
    correct: 0,  // Index of correct answer (0-3)
    verse: "The actual Bible verse text here",
    reference: "Book Chapter:Verse",
    explanation: "Additional context or explanation"
}
```

### Complete Example - English:
```javascript
{
    question: "Who was the father of Isaac?",
    answers: ["Jacob", "Abraham", "Moses", "Noah"],
    correct: 1,
    verse: "Abraham was a hundred years old when his son Isaac was born to him.",
    reference: "Genesis 21:5",
    explanation: "Abraham was the father of Isaac, who was born when Abraham was 100 years old, fulfilling God's promise."
}
```

### Complete Example - Portuguese:
```javascript
{
    question: "Quem foi o pai de Isaac?",
    answers: ["Jacob", "Abraão", "Moisés", "Noé"],
    correct: 1,
    verse: "Ora Abraão tinha cem anos, quando lhe nasceu Isaac, seu filho.",
    reference: "Génesis 21:5",
    explanation: "Abraão foi o pai de Isaac, que nasceu quando Abraão tinha 100 anos, cumprindo a promessa de Deus."
}
```

### Important Notes:
- **verse**: Use actual Bible text (can be paraphrased for clarity)
- **reference**: Book name and chapter:verse
- **explanation**: Optional but recommended - provides learning context
- Make sure to add questions to BOTH language sections for consistency

## 📝 Current Features
- ✅ Bilingual (English/Portuguese from Portugal)
- ✅ **25 questions per language** (up from 10!)
- ✅ **Bible verse references for every answer**
- ✅ **Detailed explanations** for better learning
- ✅ **Three difficulty levels** (Easy/Medium/Hard)
- ✅ **Streak tracking** to gamify learning
- ✅ Colorful, modern design
- ✅ Enhanced statistics
- ✅ Mobile responsive
- ✅ Easy to expand with more questions

## 🎨 Question Database Overview

The game now includes 25 questions covering:
- Creation and early Genesis
- Prophets and Old Testament figures
- Life of Jesus
- Miracles and teachings
- New Testament events
- Biblical facts and trivia

Each question includes scriptural backing and educational context!

## 📱 Making it a Mobile App

### For Android:
1. Use **Apache Cordova** or **Capacitor**:
   - Install Capacitor: `npm install @capacitor/cli @capacitor/core`
   - Initialize: `npx cap init`
   - Add Android: `npx cap add android`
   - Place the HTML file in the project
   - Build: `npx cap build android`

2. Or use online converters like:
   - **Appsgeyser** (easiest)
   - **Gonative.io**

### For iOS:
1. Use **Capacitor** (requires Mac):
   - Follow similar steps as Android
   - Add iOS: `npx cap add ios`
   - Build: `npx cap build ios`

### For Desktop App:
1. Use **Electron**:
   - Install: `npm install electron`
   - Create a simple electron wrapper
   - Package with: `electron-packager`

2. Or simply keep it as an HTML file that users can bookmark in their browser!

## 🎨 Customization

### Colors:
Find the `<style>` section to change colors:
- Background gradient: `background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);`
- Button colors: Look for `.language-btn`, `.answer-btn`, etc.

### Number of Questions:
The game automatically adjusts to however many questions you add!

## 📝 Current Features
- ✅ Bilingual (English/Portuguese from Portugal)
- ✅ 10 questions per language
- ✅ Colorful, modern design
- ✅ Score tracking
- ✅ Immediate feedback on answers
- ✅ Results screen with percentage
- ✅ Mobile responsive
- ✅ Easy to add more questions

## 🛠️ Technical Details
- Built with React 18
- Single HTML file (no installation needed)
- Works offline once loaded
- No backend required
- Compatible with all modern browsers

## 💡 Tips
1. Make sure English and Portuguese questions match in count for consistency
2. Always use 4 answer options
3. The `correct` index starts at 0 (not 1!)
4. Test your new questions before deploying
5. Keep questions clear and concise

Enjoy your Bible Quiz Game! ✟