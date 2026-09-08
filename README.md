# 🎯 Hangman Game

A simple and interactive **Hangman Game** built using **HTML, CSS, and JavaScript**.

The game randomly selects a word from different categories and challenges the player to guess the hidden word by selecting letters. The player has a limited number of wrong attempts before the game ends.

---

## 📌 Features

* 🎲 Randomly selects a category and word.
* 📚 Multiple categories:

  * Programming
  * Movies
  * People
  * Countries
* 🔤 Generates alphabet letters dynamically using JavaScript.
* 📝 Displays the hidden word with empty spaces.
* ✅ Reveals correctly guessed letters.
* ❌ Tracks incorrect guesses.
* 🎨 Updates the Hangman drawing based on wrong attempts.
* 🛑 Ends the game after 8 incorrect attempts.
* 💬 Displays the correct word when the game is over.
* 🖱️ Interactive letter selection.

---

## 🛠️ Technologies Used

* **HTML5** – Page structure.
* **CSS3** – Styling and Hangman drawing.
* **JavaScript (ES6)** – Game logic and DOM manipulation.

---

## 🎮 How to Play

1. Start the game.
2. A random category and word will be selected.
3. Click on any letter from the alphabet.
4. If the letter exists in the word, it will appear in its correct position.
5. If the letter is incorrect, the Hangman drawing will progress.
6. You have **8 wrong attempts**.
7. If you reach 8 wrong attempts, the game ends and the correct word is displayed.

---

## 📂 Project Structure

```text
Hangman-Game/
│
├── index.html
├── css/
│   └── style.css
│
├── js/
│   └── main.js
│
└── README.md
```

---

## 🧠 Game Logic

The game stores words in different categories using a JavaScript object:

```javascript
const words = {
  programming: [
    "php",
    "javascript",
    "go",
    "scala",
    "fortran",
    "r",
    "mysql",
    "python"
  ],

  movies: [
    "Prestige",
    "Inception",
    "Parasite",
    "Interstellar",
    "Whiplash",
    "Memento",
    "Coco",
    "Up"
  ],

  people: [
    "Albert Einstein",
    "Hitchcock",
    "Alexander",
    "Cleopatra",
    "Mahatma Ghandi"
  ],

  countries: [
    "Syria",
    "Palestine",
    "Yemen",
    "Egypt",
    "Bahrain",
    "Qatar"
  ]
};
```

JavaScript randomly selects:

1. A category.
2. A word from that category.
3. The corresponding number of empty spaces.

The selected letters are then compared with the user's guesses.

---

## 🔢 Wrong Attempts

The game allows a maximum of **8 incorrect guesses**.

Each incorrect guess adds a corresponding CSS class:

```javascript
theDraw.classList.add(`wrong-${wrongAttempts}`);
```

When the number of wrong attempts reaches 8, the game ends:

```javascript
if (wrongAttempts === 8) {
  endGame();
  lettersContainer.classList.add("finished");
}
```

---

## 📸 Game Preview

You can add screenshots of your game here:

```markdown
<img width="2732" height="1405" alt="Screenshot 2026-09-08 191512" src="https://github.com/user-attachments/assets/4c491932-94de-487b-9f99-3b4a420ddcf9" />

<img width="3340" height="1395" alt="Screenshot 2026-09-08 191406" src="https://github.com/user-attachments/assets/6c98f305-54c8-47b5-9e81-7e37366ead7f" />


```

---

## 🚀 How to Run

### Option 1: Live Server

If you're using **VS Code**:

1. Open the project folder in VS Code.
2. Install the **Live Server** extension.
3. Right-click on `index.html`.
4. Select **Open with Live Server**.

### Option 2: Browser

You can also open `index.html` directly in your browser.

---

## 👨‍💻 Author

**Omar Ahmed Sallam**

Junior Full-Stack (.NET & Angular) Developer

---

## 📄 License

This project is created for learning and practice purposes.
