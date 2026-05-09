# InvoiceDesk 🧾

A clean, fast desktop invoice generator for freelancers. Built with Electron.
Sell on Gumroad or Lemon Squeezy as a one-time purchase ($29–$39).

---

## Features
- Create, edit, save invoices locally (no cloud, no subscription)
- PDF export with one click
- Live invoice preview as you type
- Line items with qty, rate, auto totals
- Tax & discount support
- Multi-currency (USD, EUR, GBP, CAD, AUD)
- Invoice status tracking (Draft → Sent → Paid)
- Client directory built automatically
- Dashboard with revenue stats
- Search & filter invoices

---

## How to build the .exe (Windows installer)

### Prerequisites
- Node.js 18+ → https://nodejs.org
- Git (optional)

### Steps

```bash
# 1. Install dependencies
npm install

# 2. Build Windows installer (.exe)
npm run build:win

# Output will be in:  dist/InvoiceDesk Setup 1.0.0.exe  (installer)
#                     dist/InvoiceDesk 1.0.0.exe         (portable, no install needed)
```

### Build for other platforms
```bash
npm run build:mac      # macOS .dmg
npm run build:linux    # Linux .AppImage
npm run build:all      # All platforms at once
```

---

## Run in dev mode (no build)
```bash
npm install
npm start
```

---

## Project structure
```
invoicedesk/
├── main.js          # Electron main process (window, IPC, PDF export)
├── preload.js       # Secure bridge between main and renderer
├── src/
│   ├── index.html   # The full app UI (HTML/CSS/JS, no framework needed)
│   └── print.html   # PDF print template
├── assets/
│   ├── icon.png     # App icon (256x256 PNG)
│   ├── icon.ico     # Windows icon
│   └── icon.icns    # macOS icon
└── package.json
```

---

## Adding icons
Replace the placeholder files in `assets/` with real icons:
- **icon.png** — 256×256 PNG (used for Linux + fallback)
- **icon.ico** — Windows multi-size ICO file
- **icon.icns** — macOS ICNS file

Free tool to convert PNG → ICO/ICNS: https://cloudconvert.com/png-to-ico

---

## Selling on Gumroad
1. Build the `.exe` (installer version is better for buyers)
2. Go to https://gumroad.com → Create product → Digital product
3. Upload `InvoiceDesk Setup 1.0.0.exe`
4. Set price: **$29–$39** (one-time)
5. Write description (see below)
6. Publish and share!

### Suggested Gumroad description
> **InvoiceDesk** — The simplest invoice app for freelancers.
> No subscription. No cloud. Just a fast, clean desktop app that lives on your computer.
>
> ✅ Create beautiful invoices in seconds
> ✅ Export to PDF with one click
> ✅ Saves everything locally — your data stays on your machine
> ✅ Works offline, always
> ✅ One-time payment, yours forever
>
> Works on Windows 10/11.

---

## Selling on Lemon Squeezy
Same process — upload the .exe, set a one-time price, done.
Lemon Squeezy handles VAT automatically which is a bonus.

---

## Marketing ideas
- Post on r/freelance, r/webdev, r/entrepreneur
- Tweet "built in public" thread showing the app
- Post on Indie Hackers
- Make a 60-second demo video → TikTok / YouTube Shorts
- Launch on ProductHunt (free, can drive hundreds of sales)
