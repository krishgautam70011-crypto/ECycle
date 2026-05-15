<div align="center">

# ♻ E/CYCLE INDIA
### India's Premier E-Waste Management Platform

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-39d353?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Live-39d353?style=for-the-badge)

**Recycle Smarter. Live Greener.**

A fully client-side web application that lets users schedule free doorstep e-waste pickups, track their environmental impact in real time, and earn reward points for every device recycled responsibly.

[Features](#-features) · [Demo](#-demo) · [Tech Stack](#-tech-stack) · [Getting Started](#-getting-started) · [How It Works](#-how-it-works) · [Screenshots](#-screenshots) · [Contributing](#-contributing)

</div>

---

## 🌍 About The Project

India generates over **3.2 million tonnes of e-waste annually** and is the 5th largest producer of electronic waste in the world. Only 12.5% of that is formally recycled. E/CYCLE INDIA bridges that gap by making responsible e-waste disposal accessible, rewarding, and transparent for every citizen.

This project is a single-file, zero-dependency web app — no backend, no server, no database setup required. Everything runs in the browser using `localStorage` for persistence.

---

## ✨ Features

### 🏠 Home & Discovery
- **Live activity feed** — real-time submissions from the community
- **Animated hero stats** — devices recycled, kg collected, CO₂ saved, total users
- **Device Estimator** — select any of 8 device types and condition to get an instant recycling credit estimate in ₹
- **E-Waste Quiz** — 4-question interactive quiz to test environmental knowledge
- **Scrolling marquee** — live e-waste facts and statistics

### 👤 User System
- **Register & Sign In** — secure (hashed) password authentication stored locally
- **Dashboard** — personalised greeting, stats overview, recent pickups, badge collection
- **Session persistence** — stay logged in across page refreshes

### 📦 Pickup Scheduling
- **Submit a pickup** — choose device type, quantity, address, phone, and notes
- **Instant point estimate** — see how many points you'll earn before submitting
- **Unique pickup ID** — every request gets a traceable reference number

### 📊 Pickup Tracker
- **Track all pickups** — filter by status (Pending, Confirmed, Picked Up, Processing, Completed)
- **Visual progress bar** — step-by-step status pipeline for each request
- **QR Code generation** — each pickup gets a scannable QR code for verification

### 🏆 Leaderboard & Gamification
- **Animated podium** — gold / silver / bronze top 3 with glowing rings
- **Full rankings list** — all users ranked by points earned
- **Badges system** — 6 unlockable badges (First Drop, Power Saver, Metals Hero, Earth Guard, Pro Recycler, Champion)
- **Points economy** — earn points per device type and quantity recycled

### 🛠 Admin Panel
- **Password-protected** admin view
- **Status management** — move any pickup through the status pipeline
- **Summary stats** — at-a-glance count per status across all users

---

## 🚀 Demo

> Open `index.html` directly in any modern browser — no build step, no server needed.

**Demo credentials (Admin):** `admin123`

**Quick start as a user:**
1. Click **Get Started** on the homepage
2. Register with any name, email, and password
3. Submit a pickup from the dashboard
4. Watch your points and badges update live

---

## 🧰 Tech Stack

| Layer | Technology |
|---|---|
| Structure | HTML5 |
| Styling | CSS3 (custom properties, grid, animations) |
| Logic | Vanilla JavaScript (ES6+) |
| Storage | Browser `localStorage` |
| Fonts | Google Fonts — Bebas Neue, IBM Plex Mono, Outfit |
| QR Codes | [qrcodejs](https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js) via CDN |
| Icons | Emoji + inline SVG |

No frameworks. No npm. No build tools. Just one `.html` file.

---

## 📂 Project Structure

```
ecycle-india/
│
└── index.html          # Entire application — HTML + CSS + JS in one file
    ├── <style>         # ~450 lines of CSS with variables, animations, responsive design
    ├── <body>          # Views: home, auth, dashboard, submit, track, leaderboard, admin
    └── <script>        # Data layer, DB helpers, UI renderers, event handlers
```

---

## 🏁 Getting Started

### Prerequisites
- Any modern browser (Chrome, Firefox, Edge, Safari)
- No Node.js, no server, no dependencies to install

### Run Locally

```bash
# Clone the repository
git clone https://github.com/your-username/ecycle-india.git

# Navigate into the folder
cd ecycle-india

# Open in your browser
open index.html
# or on Windows
start index.html
# or just drag index.html into your browser
```

That's it. The app is fully functional.

---

## 🔄 How It Works

```
User Registers / Logs In
        ↓
Submits E-Waste Pickup Request
  → Device type, quantity, address, phone
        ↓
Pickup Enters "Pending" Status
        ↓
Admin Panel Updates Status
  Pending → Confirmed → Picked Up → Processing → Completed
        ↓
On "Completed" — Points Awarded
  → User stats updated
  → Leaderboard recalculated
  → Badges checked & unlocked
  → Global stats (kg, CO₂, devices) updated
```

### Device Points & Weights

| Device | Points | Est. Weight | Credit Range |
|---|---|---|---|
| 📲 Smartphone | 50 pts | 0.18 kg | ₹1,200 – ₹6,000 |
| 💻 Laptop | 120 pts | 2.1 kg | ₹3,500 – ₹18,000 |
| 📱 Tablet | 80 pts | 0.65 kg | ₹1,500 – ₹9,000 |
| 📺 Television | 150 pts | 8.5 kg | ₹1,000 – ₹7,000 |
| ⚡ Battery/UPS | 60 pts | 1.2 kg | ₹800 – ₹3,500 |
| 🖨️ Printer | 100 pts | 3.8 kg | ₹500 – ₹3,000 |
| ❄️ AC Unit | 200 pts | 12 kg | ₹4,000 – ₹15,000 |
| ⚙️ Other | 40 pts | 1 kg | ₹300 – ₹2,000 |

### Condition Multipliers

| Condition | Credit Multiplier |
|---|---|
| Excellent | 1.3× |
| Good | 1.0× |
| Fair | 0.65× |
| Broken | 0.25× |

---

## 🏅 Badges

| Badge | Name | Requirement |
|---|---|---|
| 🌱 | First Drop | Submit your first pickup |
| ⚡ | Power Saver | Recycle 3+ devices |
| 🔩 | Metals Hero | Recycle 5+ devices |
| 🌍 | Earth Guard | Recycle 10+ devices |
| 💎 | Pro Recycler | Earn 500+ points |
| 🏆 | Champion | Earn 1,000+ points |

---

## 📱 Responsive Design

E/CYCLE INDIA is fully responsive across all screen sizes:

| Breakpoint | Layout |
|---|---|
| Desktop (1140px+) | Full grid, side panels, 4-col device cards |
| Tablet (750–900px) | Adapted grids, hamburger nav |
| Mobile (≤750px) | Single-column, compact cards, stacked forms |
| Small (≤380px) | Optimised type sizes, minimal padding |

---

## 🌱 Environmental Impact Tracking

Every completed pickup contributes to the global counter:

- **Total devices recycled** — cumulative count across all users
- **Total kg collected** — based on device-type weight estimates
- **CO₂ saved** — calculated at 2.3 kg CO₂ per kg of e-waste properly recycled (vs landfill)

---

## 🤝 Contributing

Contributions are welcome! Here are some ways to help:

- 🐛 **Bug reports** — open an issue with steps to reproduce
- 💡 **Feature ideas** — suggest via GitHub Issues
- 🔧 **Pull requests** — fork, branch, and submit a PR

```bash
# Fork the repo, then:
git checkout -b feature/your-feature-name
git commit -m "feat: add your feature"
git push origin feature/your-feature-name
# Open a Pull Request
```

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- [QRCode.js](https://github.com/davidshimjs/qrcodejs) for QR code generation
- [Google Fonts](https://fonts.google.com) — Bebas Neue, IBM Plex Mono, Outfit
- India's e-waste statistics sourced from the Central Pollution Control Board (CPCB)

---

<div align="center">

Made with 💚 for a greener India

**[⬆ Back to top](#-ecycle-india)**

</div>
