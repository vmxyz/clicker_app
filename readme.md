# 🐾 Tamagotchi Project

## 📌 About Project

This project is a virtual pet game made with:

- HTML
- CSS
- JavaScript

The player needs to take care of the pet:
- feed it
- play with it
- let it sleep

The pet has different stats that change over time.

---

# 🎮 Game Mechanics

## Pet Stats

- Hunger
- Happiness
- Energy
- Health

All stats are limited from 0 to 100.

---

## Player Actions

### Feed
Increases hunger level.

### Play
Increases happiness.
Decreases energy.

### Sleep
Restores energy.

---

## Automatic Changes

Over time:
- hunger decreases
- happiness decreases
- energy decreases

If stats become too low, the pet becomes sad or sick.

---

# 💀 Game Over

The game ends if:
- health reaches 0
- or all stats become critically low

---

# ✨ Planned Features

- Progress bars
- Pet emotions
- Animations
- Day/Night mode
- Save system using localStorage
- Sound effects
- Different pet skins

---

# 🛠 Technologies

- HTML5
- CSS3
- Vanilla JavaScript

---

# 📂 Project Structure

```text
project-folder/
│
├── index.html
├── style.css
├── script.js
└── README.md