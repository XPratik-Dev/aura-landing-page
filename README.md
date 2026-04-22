# ✦ Aura — Build Beyond Limits

> Modern SaaS landing page. Dark-themed, animated, and fully responsive. Zero dependencies — pure HTML, CSS, and JavaScript.

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-000000?style=flat&logo=vercel&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green?style=flat)

---

## 🌐 Live Demo

**[https://aura-landing-page-one.vercel.app/](https://aura-landing-page-one.vercel.app/)**

---

## Preview

### Hero
<img width="1348" height="709" alt="Screenshot 1" src="https://github.com/user-attachments/assets/865a7fd6-b520-477b-81d6-f8bc4423d510" />

### Features — Bento Grid
<img width="1353" height="768" alt="Screenshot 2" src="https://github.com/user-attachments/assets/be3455ef-100e-4aa9-b921-6de3a8d437cb" />

### How It Works
<img width="1349" height="694" alt="Screenshot 4" src="https://github.com/user-attachments/assets/c77a0048-eb6c-4c06-ad60-9c52fa34783d" />

### Pricing
<img width="1349" height="694" alt="Screenshot 5" src="https://github.com/user-attachments/assets/84ea2397-da7e-4351-8269-21013033b6de" />

### Testimonials
<img width="1344" height="692" alt="Screenshot 6" src="https://github.com/user-attachments/assets/189fd9d0-8a35-4020-90a6-ce631127dc4c" />

### Footer
<img width="1351" height="705" alt="Screenshot 8" src="https://github.com/user-attachments/assets/4e599143-41e2-4378-aad7-1296a3e3f1df" />


---

## Features

- **Animated hero** — gradient headline, scroll-triggered stat counters, CTAs, floating dashboard mockup
- **Ambient blobs** — three animated radial blobs with blur for a glassmorphism depth effect
- **Cursor glow** — soft purple radial gradient that follows the mouse
- **Sticky navbar** — transparent on load, frosted glass on scroll with active section highlight
- **Mobile hamburger menu** — fully functional slide-down mobile nav
- **Logo marquee** — auto-scrolling trusted-by strip (Figma, Stripe, Loom, Raycast, Arc, Vercel, Linear, Notion)
- **Bento features grid** — mixed-size feature cards with live mockups inside
- **How it works** — 3-step cards with scroll-triggered reveals
- **Pricing toggle** — monthly/annual switch with live price updates
- **Testimonials** — 6 review cards with avatar initials and star ratings
- **Scroll reveal** — `IntersectionObserver` staggered fade-in on all sections
- **Active nav highlight** — current section link highlighted as you scroll

---

## File Structure

```
Aura-landing-page/
├── index.html       # All markup — 8 sections
├── style.css        # All styles — CSS variables, layout, animations
├── app.js           # All interactivity — scroll, toggle, counters, cursor
└── README.md
```

---

## Sections

| # | Section | Description |
|---|---------|-------------|
| 1 | **Navbar** | Fixed, scroll-aware, mobile-responsive |
| 2 | **Hero** | Headline, stat row, dashboard mockup |
| 3 | **Logos** | Auto-scrolling trusted-by marquee |
| 4 | **Features** | Bento-style grid with UI mockups |
| 5 | **How it works** | Connect → Build → Ship |
| 6 | **Pricing** | 3-tier cards with billing toggle |
| 7 | **Testimonials** | 6 review cards with avatars |
| 8 | **CTA + Footer** | Conversion banner + 4-column footer |

---

## Getting Started

No build step. No dependencies. No Node.js required.

**Clone and open:**
```bash
git clone https://github.com/XPratik-Dev/Aura-landing-page.git
cd Aura-landing-page
open index.html
```

**Local dev server (recommended):**
```bash
# VS Code: click "Go Live" in the bottom bar (Live Server extension)

# Or Python:
python3 -m http.server 3000
# Visit http://localhost:3000
```

---

## Customization

All design tokens are CSS variables at the top of `style.css`:

```css
:root {
  --bg:      #06060f;                    /* Page background   */
  --surface: rgba(255,255,255,.04);      /* Card surfaces     */
  --border:  rgba(255,255,255,.08);      /* Borders           */
  --purple:  #a855f7;                    /* Primary accent    */
  --cyan:    #06b6d4;                    /* Secondary accent  */
  --text:    #f8fafc;                    /* Primary text      */
  --muted:   #94a3b8;                    /* Muted text        */
  --grad:    linear-gradient(135deg, var(--purple), var(--cyan));
}
```

**Change brand color** → swap `--purple` and update `.blob-1` / `.blob-3` background colors.

**Update pricing** → find `.price-amt` spans in `index.html` and edit `data-monthly` / `data-annual` attributes.

**Add a section** → create `<section id="name">` in `index.html`, add `class="reveal"` to elements you want animated, add the nav link to both `<ul class="nav-links">` and `<div class="mobile-menu">`.

---

## JavaScript (`app.js`)

| Feature | How it works |
|---------|-------------|
| Navbar scroll effect | Adds `.scrolled` (frosted glass) after 40px scroll |
| Mobile menu | Toggles `.open` class on hamburger click |
| Scroll reveal | `IntersectionObserver` adds `.visible` with staggered delay |
| Billing toggle | Reads `data-monthly` / `data-annual` and swaps price text live |
| Active nav link | Tracks `scrollY` against each section's `offsetTop` |
| Cursor glow | Appends a fixed `div`, updates position on `mousemove` |
| Counter animation | Eased count-up fires when `.hero-stat-row` enters viewport |

---

## Deployment

Deployed on **Vercel** as a static site.

- Framework Preset: **Other**
- Build Command: *(empty)*
- Output Directory: *(empty)*
- Auto-deploys on every push to `main` via GitHub integration

🔗 **[https://aura-landing-page-one.vercel.app/](https://aura-landing-page-one.vercel.app/)**

---

## Browser Support

| Browser | Support |
|---------|---------|
| Chrome 90+ | ✅ |
| Firefox 88+ | ✅ |
| Safari 14+ | ✅ |
| Edge 90+ | ✅ |
| IE 11 | ❌ |

---

## License

MIT — free to use, modify, and ship for personal and commercial projects.

---

## Credits

- Fonts: [Inter](https://fonts.google.com/specimen/Inter) + [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans) via Google Fonts
- Design inspiration: Linear, Vercel, Framer
- Hosting: [Vercel](https://vercel.com)

---

*Built with ✦ by [XPratik-Dev](https://github.com/XPratik-Dev)*
