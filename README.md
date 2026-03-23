![Version](https://img.shields.io/badge/Version-1.2_ADV-blue)
![Hardware](https://img.shields.io/badge/Hardware-Cardputer-orange)
![Platform](https://img.shields.io/badge/Platform-M5Stack-red)
![License](https://img.shields.io/badge/License-Proprietary-gray)
[![Boosty](https://img.shields.io/badge/Support-Boosty-orange)](https://boosty.to/zeloksa)

# 🎹 Piano Tiles ADV (V1.2)

**Piano Tiles ADV** is a high-performance, 60 FPS rhythm game completely engineered and optimized from the ground up for the **M5Stack Cardputer**. It features **12** full-length 8-bit covers, dynamic difficulty scaling, new "Hold Notes" mechanics, and a custom DSP audio engine for crystal-clear piezo speaker output.

> [!IMPORTANT]
> **Source Code Status:** This project is proprietary. The source code is private. 
> **Distribution:** Binary (`.bin`) only via the **Releases** tab.

---

## ⚡ Technical Highlights

* **Cubic ADSR Audio Engine:** Custom digital signal processing applies a 120ms cubic fade-out to all square waves. This completely eliminates hardware "speaker clicks" and pops, providing a smooth, synthesizer-like retro sound.
* **Advanced Hold Notes Mechanic:** Long notes require continuous key presses. Features dynamic tile height calculation and a custom color-blending "saturate fill" (Cosmic Purple) effect based on hit-zone intersection math.
* **Hardware-Level I2C Debouncing:** Custom `holdGrace` logic prevents dropped inputs and ghosting when holding keys via the Cardputer's I2C matrix keyboard. Every physical key on a row is mapped for maximum responsiveness.
* **Dynamic Difficulty (Math-Driven):** As track progress goes from 0% to 100%, the physics engine dynamically increases tile fall speed by up to 25% while tightening the tempo.
* **SD Card Progression System:** Automatically creates a `piano_save.txt` file on your TF/SD card to permanently store your per-track High Scores and Star Ratings.
* **12 Full-Length 8-Bit Tracks:** Includes extended, multi-part arrangements of Mario, Tetris, Star Wars, Megalovania, Nyan Cat, Doom E1M1 (with dynamic bass boost), Gravity Falls, Faded, Interstellar, Rush E, Seven Nation Army, and Sweet Dreams.

---

## 🛠 Installation
1. Go to the **[Releases]** tab on the right side of this GitHub repository.
2. Download the latest **Piano Tiles ADV `.bin`** file.
3. Flash it to your M5Stack Cardputer using **M5Burner** (via the local file option) or the official **Espressif ESP32 Download Tool**.

---

## 🕹 Controls

The entire Cardputer keyboard acts as your piano. The keys are horizontally mapped to the 3 vertical lanes (including all modifier keys):
* **[ CTRL, ALT, Space, Z, X, C, V, B, N, M, ,, ., / ]** (Bottom Row): Left Lane / Menu Swipe Left
* **[ Shift, A, S, D, F, G, H, J, K, L, ;, ', Enter ]** (Middle Row): Center Lane / Menu Select
* **[ Tab, Q, W, E, R, T, Y, U, I, O, P, [, ], \ ]** (Top Row): Right Lane / Menu Swipe Right
* **[ 1, 2, 3 ... Backspace, Esc ]** (Number Row): Pause / Resume Game

---

## 📖 Comprehensive User Manual

### 🎵 Main Menu & Progression
Swipe Left/Right using the top and bottom keyboard rows to navigate the carousel. 
* Each track displays your personal **High Score (HS)** and up to **3 Stars** based on your best completion percentage (33%, 66%, and 99%).
* The title uses a mathematical Lissajous curve animation for a smooth, floating UI effect, and each track features custom 8-bit pixel art icons.

### 🎮 Gameplay Mechanics
Tiles fall down 3 distinct lanes. You must strike any key in the corresponding keyboard row before the tile passes the red hit-zone line at the bottom of the screen.
* **Hold Notes:** Tiles with a grey strip and yellow indicator must be held down until they fully cross the line. Releasing early will cost you a life.
* **Lives System:** You have 4 lives (represented by 3 hearts on screen). You are allowed 3 mistakes. Missing a tile drops a life and shatters a heart.
* **Pause Mode:** Pressing any number key pauses the game. Resuming triggers a smooth 3-second countdown timer so you can prepare your fingers.

### 💰 The Bonus Round
If you successfully survive 100% of a track, the Victory Jingle plays and you instantly enter the Bonus Round. 
* For 7 seconds, golden "Money Tiles" will rapidly fall down the screen. 
* Spam the keyboard rows to collect them. Each collected golden tile grants **+5 points** to push your High Score to the absolute limit.

### ⚙ Settings
Access the Settings menu from the first card in the carousel.
* Select `Volume` or `Brightness`.
* Tap the Left or Right keyboard rows to decrease/increase the values in increments of 15. The speaker will play a test tone when adjusting the volume.

---

## 🆕 V1.2 Changelog
* **Major Feature:** Added **Hold Notes** (long tiles) with custom visual saturation and continuous score ticking.
* **Expanded Library:** Added 5 new tracks (*Faded, Interstellar, Rush E, Seven Nation Army, Sweet Dreams*). Total tracks: 12.
* **Track Extensions:** Significantly extended the arrangements for *Megalovania, Star Wars, Gravity Falls*, and *Doom E1M1*.
* **Engine Polish:** Added I2C `holdGrace` mechanism to fix hardware button-drop during long holds. Fully mapped all physical keys to their respective lanes.
* **Bug Fixes:** Fixed instant-death bug upon track selection, perfectly centered the Pause UI, optimized text shadows.
* **Audio:** Added a dynamic +90% volume boost specifically for heavy tracks.

## 🚀 Roadmap (Upcoming in V1.3)
* **Smash Notes Mechanics:** Destructible, multi-hit heavy tiles that slow down time and require rapid button spamming to break.
* New aggressive tracks designed specifically for the Smash mechanic.

---

## 💬 Feedback & Suggestions
If you find a bug or have a suggestion for the next version:
1. Go to the **[Issues]** tab at the top of this repository.
2. Click **[New Issue]**.
3. Describe your problem or idea in detail.

---

## ☕ Support the Project
If this game brings you joy or you appreciate the technical optimization for the ESP32-S3, consider supporting further development:
* **[https://boosty.to/zeloksa](https://boosty.to/zeloksa)**

---
*Developed by Engineer Zeloksa. Strictly optimized for Cardputer ADV.*
