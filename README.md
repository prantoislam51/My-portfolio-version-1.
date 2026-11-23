# Md. Pranto Ali — Developer Portfolio

A single-file, liquid-glass personal portfolio for a full stack developer who builds web apps, ESP32 / IoT projects and explores AI. The whole site lives in one `index.html` — no build step, no framework, no dependencies to install.

> **Live site:** _add your link here after deploying (see [Deploy](#deploy-on-github-pages))_

## Highlights

- **Liquid-glass design** with an animated background, glow cursor, film grain and a scroll progress bar
- **Fixed top header** with brand, navigation and availability status; page content scrolls in its own area below it
- **Scroll-aware menu** — an indicator slides from item to item (Home → Skills → About → Projects → Blog → Contact) as you scroll
- **Two languages:** English and Bengali (বাংলা). Switching changes every visible text, including numbers
- **Uppercase mode** — one switch in Settings turns the whole site into capital letters
- **Font presets for the whole site:** 9 English and 8 Bengali presets, loaded from Google Fonts only when selected
- **Hero name** in readable italic + uppercase style with a colour shimmer
- **Skills marquee** — two rows moving in opposite directions; hovering a row pauses only that row
- **Featured projects** shown as stacking cards with demo pictures you can replace with your own
- **Settings panel** (Customize): theme (auto / light / dark), accent colour, 22 background palettes, corner style, projects layout, glass blur, and performance toggles
- **Responsive** from small phones to wide desktops; text is kept inside its cards for every font
- **Contact section** with copy-email button and a form that opens your email app with the message prefilled
- Settings are remembered in the browser (`localStorage`)

## Sections

| Section | What it shows |
| --- | --- |
| Home | Name, rotating role (Full Stack Developer, Android Developer, IoT Enthusiast, AI Learner), photo with orbiting tech icons, live ESP32 reading |
| Skills | Moving logo rows (HTML5, CSS3, JavaScript, TypeScript, React, Next.js, Astro, Tailwind CSS, Node.js, Express, MongoDB, PostgreSQL, MySQL, Python, ESP32, Arduino, Git) and three focus areas |
| About | Bio, photo, stats, Dhaka clock and a signal oscilloscope |
| Projects | ESP32 Smart Dashboard, E-Commerce Website, Attendance System, Student ID Generator |
| Process | How a project goes from idea to launch |
| Writing | Upcoming blog posts |
| Contact | Email, location, status, social links and message form |

## Tech

- HTML, CSS and vanilla JavaScript in one file
- Google Fonts (loaded on demand)
- Inline SVG for icons, logos and demo project pictures

## Demo

### Day mode

![Portfolio in day mode](<Demo Day Mod.png>)

### Light mode

![Portfolio in light mode](<Demo Light Mod.png>)

## Run locally

No installation needed.

1. Download or clone this repository
2. Open `index.html` in any modern browser

An internet connection is needed for Google Fonts. Without it the site still works and uses fallback fonts.

## Deploy on GitHub Pages

1. Create a repository and upload `index.html` and `README.md` to the root
2. Go to **Settings → Pages**
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save
4. After a minute your site is available at `https://<your-username>.github.io/<repository-name>/`

## Customize

Everything below is inside `index.html`.

**Project pictures** — near the top of the `<script>` block:

```js
var PROJECT_IMAGES={
  esp32:'',   // ESP32 Smart Dashboard
  shop:'',    // E-Commerce Website
  rfid:'',    // Attendance System
  id:''       // Student ID Generator
};
var LIVE_PREVIEW=false; // true = show animated mini-previews instead of pictures
```

Paste an image URL between the quotes. Leave it empty to keep the built-in demo picture. If a URL fails to load, the demo picture is shown instead.

**Texts and translations** — every visible string is stored in the `T` object as `[English, Bengali]`. Edit both values to change a text.

**Email address** — change the `MAIL` constant and the address shown in the two email boxes (search for `prantoislam@gmail.com`).

**Social links** — in the Contact section, replace the `https://github.com`, `https://linkedin.com`, `https://x.com` and `https://youtube.com` links with your own profiles.

**Profile photos** — the hero and About photos are embedded in the file. Replace the `src` of the two `<img>` tags with your own image URL (or a new embedded image).

**CV button** — the Download CV button currently shows a "CV file is not linked yet" message. Point it to your CV file when you have one.

**Fonts** — add or remove presets in the `FONTS` (English) and `BF` (Bengali) objects.

**Background palettes** — add colours to the `PAL` and `PALG` objects.

## File structure

```
.
├── index.html   # the whole portfolio (HTML + CSS + JS)
├── Demo Day Mod.png
├── Demo Light Mod.png
└── README.md
```

## Contact

- Email: prantoislam@gmail.com
- Location: Dhaka, Bangladesh

## License

© 2026 Md. Pranto Ali. All rights reserved. Please ask before reusing the design or content.
