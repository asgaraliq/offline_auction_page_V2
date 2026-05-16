# Offline Vehicle Auction Display System

A dynamic, fully web-based display screen designed for live, in-person vehicle auctions. This system simulates real-time bidding, complete with an automated Web Speech API auctioneer, engaging animations, and automated vehicle transition logic. It is specifically branded for **Manappuram Finance Ltd.** and conducted by **AutoBazaar Auction**.

## 🌟 Key Features

- **Automated AI Auctioneer:** Utilizes the browser's built-in Web Speech API (TTS) to provide a realistic, professional auctioneer voice with dynamic banter, bidding calls, and custom introductions.
- **Bidding Simulation:** Automatically simulates competitive bidding with randomized delays and price increments, flashing UI updates to draw attention.
- **Dynamic Lot Loading:** Seamlessly transitions between different vehicles (e.g., Hyundai Aura, Mahindra Bolero, Suzuki Gixxer) without requiring a page reload.
- **Custom Auction Scenarios:** 
  - **Success (Sold):** Triggers a "SOLD" overlay with falling confetti and a hammer bang animation.
  - **Low Bid (Passed):** Triggers a "Management Approval / Noted" scenario with custom auctioneer dialogue for vehicles not reaching their reserve price.
- **Interactive Media Gallery:** Features a thumbnail strip and a full-screen Lightbox with zoom, rotate, and keyboard navigation support.
- **Cinematic Transitions:** Includes a professional "garage door" intro curtain and animated gavel (hammer) strikes to finalize bids.

## 🚀 How to Run

Because this is a static, vanilla front-end project, it does not require a web server or backend to run locally.

1. Clone or download the project directory.
2. Open the `index.html` file in any modern web browser (Google Chrome or Microsoft Edge recommended for best TTS voice quality).
3. Click the **"Begin Auction"** button on the initial overlay. 
   > *Note: Browsers block automatic audio playback. Clicking this button unlocks the Web Speech API and starts the introductory sequence.*

## 🛠 Technologies Used

- **HTML5:** Semantic structure and layout.
- **CSS3:** Custom styling, CSS Grid, Flexbox, UI animations, and glassmorphism overlays.
- **JavaScript (ES6+):** Core application logic, DOM manipulation, asynchronous timing, and Web Speech API integration.
- **Canvas Confetti:** A lightweight third-party library (`confetti.browser.min.js`) for the "Sold" celebration effect.

## 📁 Project Structure

```text
offline_auction_page_V2/
│
├── index.html                   # Main application file (UI + Logic)
├── README.md                    # Project documentation
│
├── logo/
│   └── manpurram_logo.png       # Brand logos
│
├── icons/
│   └── *.svg                    # UI icons (specs, condition, etc.)
│
└── vehicle_images/
    ├── Vehicel_1/               # Images for Lot #1 (Hyundai AURA)
    ├── Vehicel_2/               # Images for Lot #2 (Mahindra BOLERO)
    └── Vehicle_3/               # Images for Lot #3 (Suzuki GIXXER)
```

## ⚙️ Customization

- **Bidding Logic:** You can adjust the random delays (`nextBidTicks`) or bid increments inside the `auctionTick()` function in `index.html`.
- **Audio Voice:** The `speak()` function attempts to target an Indian Male voice (`Ravi`, `Rishi`, or `Heera`) depending on the operating system. You can change these parameters to switch the voice type.
- **Adding Vehicles:** To add more vehicles, extend the `loadNextVehicle()` function logic in `index.html` by creating new `currentVehicleIndex` conditions and mapping them to new image folders.

---
*Developed for AutoBazaar & Manappuram Finance Ltd. Offline Auction Events.*