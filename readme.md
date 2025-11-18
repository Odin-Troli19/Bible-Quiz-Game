# Bible Quiz Game - Instructions

## 📖 Overview
A bilingual (English/Portuguese) Bible quiz game that works on both desktop and mobile devices.

## 🎮 How to Use

### Desktop:
1. Simply double-click `bible-quiz-game.html` to open it in your browser
2. Or right-click → Open with → Your preferred browser

### Mobile:
1. Transfer the HTML file to your phone
2. Open it with any mobile browser (Chrome, Safari, Firefox, etc.)

## ➕ How to Add More Questions

Open `bible-quiz-game.html` in any text editor and find the `questionsDatabase` section (around line 265). 

### Format for English Questions:
```javascript
{
    question: "Your question here?",
    answers: ["Option 1", "Option 2", "Option 3", "Option 4"],
    correct: 0  // Index of correct answer (0 = first, 1 = second, 2 = third, 3 = fourth)
}
```

### Format for Portuguese Questions:
```javascript
{
    question: "A tua pergunta aqui?",
    answers: ["Opção 1", "Opção 2", "Opção 3", "Opção 4"],
    correct: 0  // Índice da resposta correcta (0 = primeira, 1 = segunda, 2 = terceira, 3 = quarta)
}
```

### Example - Adding a New Question:

**English Section** (find `en: [` around line 267):
```javascript
en: [
    // ... existing questions ...
    {
        question: "Who was the mother of Jesus?",
        answers: ["Elizabeth", "Mary", "Martha", "Sarah"],
        correct: 1
    },
    // Add more here
]
```

**Portuguese Section** (find `pt: [` around line 309):
```javascript
pt: [
    // ... existing questions ...
    {
        question: "Quem era a mãe de Jesus?",
        answers: ["Isabel", "Maria", "Marta", "Sara"],
        correct: 1
    },
    // Add more here
]
```

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