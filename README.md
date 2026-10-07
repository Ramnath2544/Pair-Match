# 🧠 Pair Match Game

> A fun, interactive and visually engaging **Memory Card Matching Game** built with pure **HTML, CSS and JavaScript**.

Test your memory, find all matching pairs, and try to beat your **best score**! 🎯

---

## 🎮 Live Preview

### 🃏 Memory Match

Flip the cards, remember their positions, and match all **8 pairs** using the fewest possible moves.

✨ **Can you beat your best score?**

---

## ✨ Features

- 🧠 **Memory-based gameplay**
- 🃏 **16 interactive cards**
- 🎯 **8 unique matching pairs**
- 🔀 **Random card shuffling**
- 🔄 **3D card flip animation**
- 🏆 **Best score tracking**
- 💾 **LocalStorage support**
- 🔁 **Restart Game option**
- 🗑️ **Clear Best Score option**
- 🔒 **Prevents accidental double-clicking**
- ⏳ **Automatic card flip-back after an incorrect match**
- 🎨 **Modern glassmorphism UI**
- 🌈 **Gradient background**
- ✨ **Animated game title**
- 📱 **Responsive layout**

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| 🌐 HTML5 | Game structure |
| 🎨 CSS3 | Styling & animations |
| ⚡ JavaScript | Game logic |
| 💾 LocalStorage | Saving best score |
| 🔀 Fisher-Yates Shuffle | Randomizing cards |

---

## 🎯 How to Play

### 1️⃣ Start the Game

Open the game in your browser.

You will see **16 face-down cards**.

### 2️⃣ Flip a Card

Click any card to reveal its emoji.

### 3️⃣ Find Its Match

Click another card.

- ✅ If the cards match → they remain open.
- ❌ If they don't match → they automatically flip back.

### 4️⃣ Complete the Board

Continue matching cards until all **8 pairs** are found.

### 5️⃣ Beat Your Best Score

The game counts the number of moves you make.

Your **lowest number of moves** is stored as your Best Score.

---

## 🏆 Scoring System

The objective is simple:

> **Complete the game using the fewest moves possible.**

For example:

```text
Moves: 12
Best: 12
```

If you later complete the game in fewer moves:

```text
Moves: 10
Best: 10 🎉
```

Your best score is automatically saved in your browser using:

```javascript
localStorage
```

---

## 🎨 Game UI

The game uses a modern **glassmorphism-inspired design** with:

- 🌌 Gradient background
- 🪟 Transparent glass container
- 💫 Shadow effects
- 🔄 3D card flipping
- ✨ Animated title
- 🟡 Highlighted matched cards
- 🎯 Interactive buttons

---

## 🧩 Game Architecture

The game is divided into three main parts:

```text
Memory Match Game
│
├── HTML
│   ├── Game Container
│   ├── Score Board
│   ├── Game Status
│   ├── Card Board
│   └── Control Buttons
│
├── CSS
│   ├── Glassmorphism UI
│   ├── Gradient Background
│   ├── Card Design
│   ├── 3D Flip Animation
│   └── Button Animations
│
└── JavaScript
    ├── Card Creation
    ├── Card Shuffling
    ├── Card Flipping
    ├── Match Detection
    ├── Move Counter
    ├── Best Score
    └── LocalStorage
```

---

## 🧠 Core Game Logic

The game creates pairs from the following emojis:

```javascript
const emojis = [
  '🌟',
  '🚀',
  '🎸',
  '💎',
  '🌈',
  '🔥',
  '🧩',
  '🍔'
];
```

The array is duplicated to create 16 cards:

```javascript
let cardsArray = [...emojis, ...emojis];
```

The cards are then randomly shuffled before every game.

---

## 🔀 Card Shuffling

The project uses the **Fisher-Yates Shuffle Algorithm**:

```javascript
function shuffleCards() {
  for (let i = cardsArray.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));

    [cardsArray[i], cardsArray[j]] =
      [cardsArray[j], cardsArray[i]];
  }
}
```

This ensures that the cards appear in a different order every time the game starts.

---

## 🔄 3D Card Flip

The card flipping effect is created using CSS:

```css
.card.flip {
  transform: rotateY(180deg);
}
```

The game uses:

```css
transform-style: preserve-3d;
```

and:

```css
backface-visibility: hidden;
```

to create the 3D flipping animation.

---

## 💾 Best Score

The best score is stored in the browser:

```javascript
localStorage.setItem(
  'memoryMatchBestScore',
  bestScore
);
```

It can later be retrieved using:

```javascript
localStorage.getItem(
  'memoryMatchBestScore'
);
```

This means your best score remains available even after refreshing the page.

---

## 📂 Project Structure

```text
memory-match-game/
│
├── index.html
└── README.md
```

Since the project is built using vanilla HTML, CSS and JavaScript, **no installation or external dependencies are required**.

---

## 🚀 Getting Started

### Step 1 — Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/memory-match-game.git
```

### Step 2 — Open the Project

```bash
cd memory-match-game
```

### Step 3 — Run the Game

Simply open:

```text
index.html
```

in your browser.

### Recommended

You can also use **VS Code + Live Server** for development.

---

## 🌐 Run Locally

You don't need:

```text
Node.js
npm
React
MongoDB
Backend
Database
```

Just:

```text
HTML + CSS + JavaScript
```

That's it! 🚀

---

## 📸 Game Preview

Add your game screenshot here:

```markdown
![Memory Match Game Preview](./assets/game-preview.png)
```

Recommended project structure:

```text
memory-match-game/
│
├── index.html
├── README.md
│
└── assets/
    └── game-preview.png
```

---

## 💡 Future Improvements

Some exciting features that can be added:

- ⏱️ Game timer
- ❤️ Lives system
- 🔊 Sound effects
- 🎵 Background music
- 🌙 Dark/Light mode
- 📊 Game statistics
- 🥇 Leaderboard
- 🎚️ Difficulty levels
- 🃏 6×6 and 8×8 boards
- 👥 Multiplayer mode
- 📱 Improved mobile controls
- 🎉 Confetti animation after winning
- 🏅 Achievement system

---

## 🎚️ Possible Difficulty Levels

| Level | Board | Pairs |
|---|---:|---:|
| 🟢 Easy | 4 × 4 | 8 |
| 🟡 Medium | 6 × 6 | 18 |
| 🔴 Hard | 8 × 8 | 32 |

---

## 🧑‍💻 Learning Outcomes

This project is a great beginner-to-intermediate JavaScript project because it demonstrates:

- DOM Manipulation
- Event Listeners
- JavaScript Arrays
- Array Destructuring
- Randomization
- Functions
- Conditional Statements
- CSS Animations
- CSS 3D Transforms
- Data Attributes
- `setTimeout()`
- Browser LocalStorage
- Game State Management

---

## 🧠 Important JavaScript Concepts

The project demonstrates several real-world JavaScript concepts:

```javascript
document.querySelector()
```

```javascript
document.createElement()
```

```javascript
addEventListener()
```

```javascript
classList.add()
```

```javascript
classList.remove()
```

```javascript
setTimeout()
```

```javascript
localStorage.setItem()
```

```javascript
localStorage.getItem()
```

These concepts are useful for building interactive web applications.

---

## 🤝 Contributing

Contributions are welcome! 🎉

### 1. Fork the repository

```text
Fork → Clone → Modify → Commit → Push → Pull Request
```

### 2. Create a new branch

```bash
git checkout -b feature/new-feature
```

### 3. Commit your changes

```bash
git add .
git commit -m "Add new feature"
```

### 4. Push the branch

```bash
git push origin feature/new-feature
```

### 5. Create a Pull Request 🚀

---

## ⭐ Support

If you enjoyed this project, consider giving the repository a ⭐ on GitHub.

It helps support the project and encourages further development!

---

## 📜 License

This project is open-source and available under the **MIT License**.

---

## 👨‍💻 Author

**Ramnath**

Computer Science & Technology Enthusiast

> 💻 Building projects, learning technology, and solving problems.

---

<div align="center">

### 🧠 Test Your Memory. 🎯 Beat Your Score. 🏆 Have Fun.

**Made with ❤️ using HTML, CSS & JavaScript**

⭐ **If you like this project, don't forget to star the repository!** ⭐

</div>
