![Version](https://img.shields.io/badge/Version-2.0_ADV-blue)
![Hardware](https://img.shields.io/badge/Hardware-Cardputer-orange)
![Platform](https://img.shields.io/badge/Platform-M5Stack-red)
![License](https://img.shields.io/badge/License-Proprietary-gray)
[![Boosty](https://img.shields.io/badge/Support-Boosty-orange)](https://boosty.to/zeloksa)

# 🎹 Piano Tiles ADV (V2.0)

**Piano Tiles ADV** is a high-performance, 60 FPS rhythm game completely engineered and optimized from the ground up for the **M5Stack Cardputer**. Now featuring a massive library of **54** full-length tracks across **5 Themed Music Packs**, dynamic difficulty scaling, "Hold Notes" mechanics, immersive animated backgrounds, and a custom DSP audio engine for crystal-clear piezo speaker output.

> [!IMPORTANT]
> **Source Code Status:** This project is proprietary. The source code is private. 
> **Distribution:** Binary (`.bin`) only via the **Releases** tab.

---

## ⚡ Technical Highlights

* **Massive 54-Track Library:** Play through 5 themed packs: *Classics*, *Anime Hits*, *Gaming Legends*, *Movie Epics*, and *Rock Legends*. Every track is a full-length, high-scoring arrangement (80 to 120+ notes).
* **Advanced Hold Notes Mechanic:** Long notes require continuous key presses. Features dynamic tile height calculation and a custom color-blending "saturate fill" (Cosmic Purple) effect based on hit-zone intersection math.
* **Immersive Visuals & UI:** Features 5 distinct animated backgrounds (Synthwave Grid, Cherry Blossoms, Digital Matrix, Film Strip, Concert Lasers), dynamic pack selection UI, and custom 8-bit pixel art icons for every single track.
* **Hardware-Level I2C Debouncing:** Custom `holdGrace` logic prevents dropped inputs and ghosting when holding keys via the Cardputer's I2C matrix keyboard. Every physical key on a row is mapped for maximum responsiveness.
* **Dynamic Difficulty (Math-Driven):** As track progress goes from 0% to 100%, the physics engine dynamically increases tile fall speed by up to 25% while tightening the tempo.
* **SD Card Progression System:** Automatically creates a `piano_save.txt` file on your TF/SD card to permanently store your per-track High Scores, Star Ratings, and overall pack completion.

---

## 🛠 Installation

### Method 1: M5Burner (Recommended)
1. Open **M5Burner**.
2. Search for `Piano Tiles ADV` or `Zeloksa`.
3. Select version **V2.0**.
4. Burn to your M5Stack Cardputer.

### Method 2: Manual Flashing
1. Go to the **[Releases]** tab on the right side of this GitHub repository.
2. Download the latest **Piano Tiles ADV `.bin`** file.
3. Flash the `.bin` to your M5Stack Cardputer using **M5Burner** (via the local file option) or the official **Espressif ESP32 Download Tool**.

---

## 🕹 Controls

The entire Cardputer keyboard acts as your piano. The keys are horizontally mapped to the 3 vertical lanes (including all modifier keys):
* **[ CTRL, ALT, Space, Z, X, C, V, B, N, M, ,, ., / ]** (Bottom Row): Left Lane / Menu Swipe Left
* **[ Shift, A, S, D, F, G, H, J, K, L, ;, ', Enter ]** (Middle Row): Center Lane / Menu Select
* **[ Tab, Q, W, E, R, T, Y, U, I, O, P, [, ], \ ]** (Top Row): Right Lane / Menu Swipe Right
* **[ 1, 2, 3 ... Backspace, Esc ]** (Number Row): Pause / Resume Game / Exit Track Select

---

## 📖 Comprehensive User Manual

### 🎵 Main Menu & Progression
Swipe Left/Right using the top and bottom keyboard rows to navigate between the **5 Music Packs** and Settings. 
* Press the Middle Row to enter a Pack.
* Each pack displays an **Animated Emoji** reflecting your overall completion percentage (from sleeping to starry-eyed!).
* Inside a pack, each track displays your personal **High Score (HS)** and up to **3 Stars** based on your best completion percentage (33%, 66%, and 99%).
* Each Pack has its own unique background music and animated background that matches the theme.

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

## 🆕 V2.0 Massive Expansion Update
* **5 Themed Music Packs:** Classics, Anime Hits, Gaming Legends, Movie Epics, and Rock Legends.
* **54 Tracks Total:** Added 40 new tracks! Featuring Master Difficulty arrangements for Tokyo Ghoul, Evangelion, Halo, Portal, Pirates of the Caribbean, AC/DC, Queen, and dozens more. 
* **Complete Overhaul of Track Lengths:** Every track has been rewritten and extended. You can now score a minimum of 1000 points on every single song.
* **Animated Backgrounds:** 5 custom dynamic backgrounds tied to each pack (Retro Grid, Falling Sakura, Digital Matrix, Scrolling Film, Concert Lasers).
* **Thematic Background Music:** 5 unique BGM loops that play while navigating the track selection menus.
* **Progress Emojis:** A new procedural emoji face tracks your completion rate for each pack in real-time.
* **UI & Visual Upgrades:** 54 ultra-detailed, multi-layered 8-bit icons. Improved UI animations and smoother track carousel navigation.

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
