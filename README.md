# 🏐 Volleyball Lineup

A standalone, mobile-optimized web application designed for volleyball coaches and team captains to effortlessly manage rosters, draft perfectly balanced teams, and share lineups instantly. 

Built entirely with HTML, CSS, and Vanilla JavaScript, this app runs entirely in the browser and saves all data locally to the device—no database or internet connection required after the initial load.

## ✨ Features

* **Intelligent Auto-Generator:** Uses a custom "Weakest-First Specialist Draft" algorithm. It evaluates players based on High/Mid/Low tier priorities, ensuring specialists get their preferred roles while saving highly versatile players to fill difficult gaps later.
* **Smart Drag & Drop:** Intuitive touch controls allow you to drag players onto the court. Dropping a player onto an occupied zone automatically swaps them with the existing player.
* **Instant Redrafting:** If exactly 12 players are on the court, hitting the Auto-Gen button skips the selection menu and instantly reshuffles the teams for a fresh, mathematically balanced matchup.
* **WhatsApp Share Integration:** Features a built-in screenshot engine (`html2canvas`) that crops out the bench, captures the scoreboard and court, and opens your native mobile share sheet to send the lineup directly to your team chat.
* **Persistent Local Storage:** Closes the app? Refreshing the page? Your entire 30-player roster, court layout, and scores are saved instantly to your browser's local storage. 
* **Custom Scoreboard:** Tap-to-edit team names and scores that capture perfectly in exported screenshots without breaking RTL (Right-to-Left) Arabic text formatting.

## 📱 How to Install (Mobile)

Since this is a Progressive Web App (PWA) style single-page application, you do not need an app store to install it.

1. Open the live hosted link on your mobile browser (Safari, Chrome, or Samsung Internet).
2. Tap the browser's share or menu icon.
3. Select **"Add to Home Screen"**.
4. The app will now live on your phone like a native application and will run in full-screen mode.

## 🛠️ Position Priority System

When adding a player, you do not use arbitrary "power ratings." Instead, you assign their preferred positions into three tiers:
* **High Priority**
* **Mid Priority**
* **Low Priority**

The Auto-Gen algorithm reads these tiers from left to right (Rank 1 through 5) and drafts the 12 selected players into perfectly mirrored Home and Guest sides, prioritizing Setters (S) and Mid Receivers (MR) first.

## 💻 Tech Stack

* **Frontend:** HTML5, CSS3, Vanilla JavaScript (ES6+)
* **Dependencies:** [html2canvas](https://html2canvas.hertzen.com/) (For screenshot generation)
* **Storage:** `localStorage` API
