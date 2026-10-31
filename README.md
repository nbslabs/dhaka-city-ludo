# Dhaka City 3D Ludo

A culturally immersive, browser-based 3D Ludo board game
set on a Dhaka rooftop ("Chhad"). Built entirely as a
single-page web app with Three.js and Tone.js, it brings
the nostalgic experience of playing Ludo during a rooftop
"adda" to life - complete with rickshaw bells, CNG buzzes,
street food vendors, Kalboishakhi storms, and a full
first-person rooftop exploration mode.

🌐 **Live Demo:**
[dhakaludo.nbslabs.dev](https://dhakaludo.nbslabs.dev)

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Social Sharing & Virality](#social-sharing--virality)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Gameplay Guide](#gameplay-guide)
- [Camera Modes](#camera-modes)
- [Dhaka Twist Events](#dhaka-twist-events)
- [FPS Rooftop Explorer](#fps-rooftop-explorer)
- [Weather System](#weather-system)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

Dhaka City 3D Ludo reimagines the classic Ludo board game
through the lens of Dhaka's vibrant street culture. Four
teams - each representing an iconic piece of the city -
compete on a Ludo board placed on a detailed 3D Dhaka
rooftop. The game features a full AI opponent, procedural
audio soundscapes, dynamic weather, and an explorable
first-person mode where you can walk around the rooftop,
interact with street food vendors, fly kites, and shoot
traditional Bengali toys.

**Who is it for?**

- Bangladeshi diaspora looking for a nostalgia trip
- Ludo fans wanting a visually rich, themed experience
- Anyone curious about Dhaka's rooftop culture

---

## Features

- **3D WebGL Board** - Full Three.js-powered Ludo board
  with shadows, fog, and procedural geometry on an
  octagonal Dhaka rooftop
- **4 Dhaka-Themed Teams** - Lalbagh Rickshaw (Red),
  Dhanmondi CNG (Green), Sonargaon Tiger (Yellow), and
  Buriganga Launch (Blue), each with unique sound effects
- **4 Game Modes** - 1P vs AI, 2P Local, 4P Local,
  and Online 2P (peer-to-peer via WebRTC)
- **Smart AI Opponent** - Heuristic-based AI that
  prioritizes captures, safe squares, and home stretches
- **Procedural Audio Engine** - Real-time Tone.js
  soundscape with metro rail Doppler, diesel bus rumble,
  CNG putt-putt, rickshaw bells, and ambient BGM
- **11 Weather Presets** - Morning, Noon, Sunny, Afternoon,
  Evening, Night, Midnight, Full Moon, Rainy, Kalboishakhi
  Storm (with lightning and flood waves), and Snowy
- **14+ Dhaka Twist Events** - Traffic Jams, Load Shedding,
  Shantinagar Floods, WASA Digging, Mosquito Fogger,
  Rooftop Cat, Pigeon Frenzy, Tank Overflow, Achar Drying,
  Qurbani Cow, Cricket Sixer, Monkey Troop, and more
- **First-Person Rooftop Walk** - Full FPS mode with WASD
  movement, sprint, jump, and collision physics
- **12 Interactive NPC Spots** - Tong Cha stall, Fuchka
  cart, Jhalmuri vendor, Paan kiosk, Kacchi Biriyani chef,
  BBQ grill, Guitar Adda, Bioscope box, Traffic Sergeant,
  Kite Flyers, and a Toy Store
- **Toy Store & Projectile System** - Buy and shoot
  traditional toys: Batul (slingshot with clay guli),
  bamboo bow and arrows, Paperfly planes, Latim (spinning
  tops), Patka (firecrackers), and Fanush (sky lanterns)
- **Rooftop Disco Party** - 10-second dance party mode with
  a disco ball, color beams, and beat-synced music
- **Tank Overflow Mini-Game** - Emergency pump switch
  mechanic where the rooftop floods and the board gets
  washed away if you don't act in time
- **Bilingual UI** - Bengali and English throughout the
  interface, dialogues, and toast notifications
- **Mobile Responsive** - Touch-optimized with adaptive UI
  for phones and tablets, virtual D-pad, and action buttons
- **Online Multiplayer** - Peer-to-peer via PeerJS/WebRTC
  DataChannels, no backend server needed. Share a 6-character
  room code via WhatsApp or Messenger to connect
- **Victory Shareable Card** - Auto-generated canvas-based
  victory card with player stats, Bangla taglines, and
  one-tap sharing to WhatsApp, Facebook, X/Twitter, or
  native share
- **📸 Chhad Moment Screenshot** - One-click clean 3D scene
  capture with branded watermark, camera shutter sound, and
  instant sharing (press **P** or the camera button)
- **🌦️ Dhaka Weather Postcard** - Transform any screenshot
  into a vintage postcard with weather-specific Bangla
  captions, decorative stamp, paper texture, and corner
  flourishes
- **🎯 Challenge a Friend Deep Link** - Generate a challenge
  URL after winning, share via WhatsApp with Bangla
  trash-talk, and your friend auto-joins your room from the
  link
- **Google Analytics** - Integrated page-level tracking

---

## Social Sharing & Virality

The game includes a complete social sharing toolkit designed
to drive organic growth via WhatsApp, Messenger, and social
media - the dominant sharing platforms in Bangladesh.

### 🏆 Victory Shareable Card

After winning, an auto-generated **1080x1080 canvas card**
includes:

- Player's team name, icon, and color gradient background
- Win stats: Rolls, Chhakkas (sixes), and Captures
- A randomly selected Bangla tagline (e.g. "ছাদের লুডুতে
  চ্যাম্পিয়ন! 🏅")
- Game logo and URL watermark
- Share buttons: WhatsApp, Facebook, X/Twitter, Download,
  and native Web Share API with image attachment

### 📸 Chhad Moment Screenshot

A camera button in the HUD (or press **P**) captures a
clean screenshot of the 3D rooftop scene:

- All UI overlays are temporarily hidden for a clean frame
- A forced WebGL render pass captures the current scene
- A branded watermark is composited with the game title,
  current weather, camera mode, timestamp, and domain
- Synthesized camera shutter sound provides audio feedback
- Share via WhatsApp, X/Twitter, download, or native share

### 🌦️ Dhaka Weather Postcard

Toggle the "📮 Make Postcard" button in the screenshot modal
to transform any capture into a vintage-style postcard:

- **1440x1080** landscape layout with cream paper texture
  and grain noise
- Scene photo with white border, drop shadow, and vignette
- **Weather-specific Bangla captions**, for example:
  - Morning: "ঢাকার সকালে ছাদে চা আর লুডু ☕"
  - Evening: "ঢাকার সন্ধ্যায় ছাদে লুডু আড্ডা 🌇"
  - Rainy: "বৃষ্টির দিনে ছাদে বসে খেলা 🌧️"
  - Kalboishakhi: "কালবৈশাখীর ঝড়ে ছাদে লুডু! ⛈️"
- Decorative perforated stamp with dice icon and game
  branding
- Corner flourishes and "From the Chhad, Dhaka" tagline

### 🎯 Challenge a Friend Deep Link

After any victory, click "CHALLENGE A FRIEND" to:

1. Generate a unique URL like
   `dhakaludo.nbslabs.dev/?challenge=ABC123`
2. Start hosting a PeerJS room with that code
3. Share via WhatsApp with Bangla trash-talk messages, e.g.:
   > "আমি ছাদের লুডুতে ৬ গেম জিতেছি! তোর সাহস থাকলে আয়,
   > অনলাইনে খেল! 🎲🔥"
4. When your friend opens the link, the game auto-joins
   the room - no manual code entry needed
5. Win counter is tracked in `localStorage` and included in
   challenge messages

---

## Tech Stack

| Layer         | Technology                          |
| ------------- | ----------------------------------- |
| Language      | HTML, CSS, JavaScript (Vanilla)     |
| 3D Engine     | Three.js r128                       |
| Audio Engine  | Tone.js 14.8                        |
| P2P Network   | PeerJS 1.5 (WebRTC DataChannels)    |
| CSS Framework | Tailwind CSS (CDN)                  |
| Fonts         | Google Fonts (Cinzel, Inter, Rozha) |
| Icons         | Material Symbols Rounded            |
| Hosting       | GitHub Pages (Custom Domain)        |
| Analytics     | Google Analytics (gtag.js)          |

---

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- No build tools, package managers, or servers required

### Run Locally

1. **Clone the repository:**

   ```bash
   git clone git@github.com:nbslabs/dhaka-city-ludo.git
   cd dhaka-city-ludo
   ```

2. **Open in browser:**

   Simply open `index.html` in your browser, or use any
   local HTTP server:

   ```bash
   # Using Python
   python3 -m http.server 8000

   # Using Node.js (npx)
   npx -y serve .
   ```

3. **Visit** `http://localhost:8000` in your browser.

> **Note:** WebGL support is required. For the best
> experience, use a Chromium-based browser with hardware
> acceleration enabled.

---

## Gameplay Guide

### Starting a Match

1. **Select Game Mode** - Choose between 1P vs AI,
   2P Local, 4P Local, or Online 2P
2. **Choose Your Team** - Pick from the four Dhaka teams
3. **Press START** to begin

### Online Multiplayer

1. Select **🌐 Online** from the game mode selector
2. **Create Room** - A 6-character room code is generated.
   Share it with your friend via WhatsApp, Messenger, or
   any chat app
3. **Join Room** - Your friend pastes the code and clicks
   Connect
4. Once connected, the host clicks **START ONLINE MATCH**
5. The game syncs dice rolls, piece moves, and Dhaka Twist
   events in real-time over a direct WebRTC DataChannel

> **Note:** Both players must have internet access for the
> initial WebRTC handshake. After connecting, game data
> flows directly between browsers with no server.

### Rules

- Standard Ludo rules apply on a 52-tile perimeter track
  with 4 pieces ("Gutis") per team
- Roll a **6** to bring a Guti out of "Ghor" (home base)
- Land on an opponent's Guti to capture and send it back
- Navigate through 6 safe star tiles marked on the track
- Enter your **home stretch** and reach **Shapla Chattar**
  (the central monument) to score
- First team to get all 4 Gutis to Shapla Chattar wins
- Rolling a 6, capturing, or scoring grants a bonus turn
- 4 busy Dhaka junctions (New Market Mor, Farmgate Box,
  Bijoy Sarani, Shahbagh Mor) add strategic depth

### Dice

Roll the artisanal 2D die by clicking the "Roll Dice"
button or tapping it on mobile. The die displays classic
pip patterns with a red center dot.

---

## Camera Modes

Cycle through views with the **V** key or the camera button
in the HUD:

| Mode       | Description                          |
| ---------- | ------------------------------------ |
| Chhad View | Default 3D orbit, drag to rotate     |
| Top View   | Bird's-eye overhead view of the board|
| FPS Walk   | First-person rooftop exploration     |

---

## Dhaka Twist Events

Trigger random Dhaka-themed events using the **Dhaka Twist**
button in the HUD. These events affect gameplay and add
immersive chaos:

| Event                | Effect                               |
| -------------------- | ------------------------------------ |
| Traffic Jam          | Blocks a junction tile temporarily   |
| Load Shedding        | Dims lights, candle-lit ambience     |
| Shantinagar Flood    | Waterlogged tile slows non-boat Gutis|
| WASA Digging         | Trench blocks a tile on the track    |
| Mosquito Fogger      | Fogger cloud obscures part of board  |
| Rooftop Cat          | Stray cat blocks a tile              |
| Pigeon Frenzy        | Pigeons scatter across the board     |
| Tank Overflow        | Emergency pump mini-game             |
| Achar Drying         | Pickle mat blocks a tile             |
| Qurbani Cow          | Animated cow obstacle on the board   |
| Cricket Sixer        | Speed boost tile appears             |
| Monkey Troop         | Banana-peel slip hazard tiles        |
| Nostalgia Hawker     | Vintage bioscope moment              |

---

## FPS Rooftop Explorer

In FPS mode, walk around the fully realized Dhaka rooftop:

### Controls

| Key / Input         | Action                        |
| ------------------- | ----------------------------- |
| WASD / Arrow Keys   | Walk                          |
| Shift (hold)        | Sprint                        |
| Spacebar            | Jump                          |
| E                   | Interact with NPC / vendor    |
| F / Left Click      | Shoot or launch equipped toy  |
| Keys 1-6            | Switch equipped toy           |
| V                   | Switch camera mode            |
| P                   | Capture Chhad Moment screenshot |
| Mouse / Touch Drag  | Look around                   |

### Interactive Spots

- **Tong Cha Stall** - Order Malai Cha for a speed boost
- **Fuchka Cart** - Eat spicy Naga Fuchka for a sprint
- **Jhalmuri Cart** - Grab Jhalmuri with mustard oil
- **Paan Kiosk** - Try Old Dhaka Meetha Paan
- **Kacchi Biriyani Chef** - Get a mega energy boost
- **BBQ Grill** - Taste smoky Shik Kabab
- **Guitar Adda** - Join a rooftop acoustic jam session
- **Bioscope Box** - Peer into a vintage peep-show
- **Traffic Sergeant** - Toggle the flyover traffic signal
- **Kite Flyers** - Shout "Bho-Katta!" during Shakrain
- **Toy Store** - Buy Batul, Dhonuk, Paperfly, Latim,
  Patka, and Fanush to shoot across the rooftop

---

## Weather System

The game features a dynamic weather cycle with 11 presets
that affect lighting, sky color, fog density, particle
effects, and ambient sound:

- **Auto Cycle** - Weather changes every ~18 seconds
- **Manual Override** - Click the weather button to lock a
  specific preset
- **Kalboishakhi Storm** - Features procedural lightning
  bolts, rolling storm clouds, rooftop flood waves, and
  NPCs running to shelter
- **Snowy** - Snowfall particles for a whimsical touch

---

## Project Structure

```
dhaka-city-ludo/
├── index.html    # Entire application (HTML + CSS + JS)
├── logo.png      # Game logo (used in start overlay)
├── base-menu.png # Menu background image
├── CNAME         # Custom domain for GitHub Pages
├── LICENSE       # MIT License
└── README.md     # This file
```

The project is a single self-contained HTML file (~14,700
lines, ~754 KB) that includes:

- Inline CSS with Tailwind CDN and custom styles
- Full Three.js 3D scene (board, rooftop, city environment,
  weather, disco rig, NPC spots, toy projectiles)
- Procedural audio engine (CathedralAudio class) using
  Tone.js with 30+ synthesized sound effects
- Complete game logic (dice, moves, captures, AI, events)
- FPS mode with collision, jump physics, and NPC dialogue
- Social sharing system (Victory Card, Screenshot, Postcard,
  Challenge Deep Links)
- Online P2P multiplayer via PeerJS/WebRTC
- Responsive touch and keyboard input handling

---

## Contributing

Contributions are welcome! Here are some ways to help:

1. **Fork** the repository
2. **Create a branch** for your feature or fix
3. **Make your changes** and test locally
4. **Submit a Pull Request** with a clear description

### Ideas for Contributions

- Additional Dhaka Twist events
- More FPS-mode interactable vendors and items
- Performance optimizations for mobile devices
- Accessibility improvements
- Localization for additional languages
- Replay GIF/video clip system for dramatic moments
- Weekly leaderboard badge system
- Bangla trash-talk sticker pack

---

## License

This project is licensed under the
[MIT License](LICENSE).

---

<p align="center">
  Built with ❤️ for Dhaka by
  <a href="https://github.com/nbslabs">NBS Labs</a>
</p>
