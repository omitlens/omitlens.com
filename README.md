# OmitLens

> Through our creations, we shape experiences that embrace imperfection and the blurred boundaries between things — where meaning often hides.

**Website:** [omitlens.com](https://omitlens.com)

## Overview

OmitLens is a collection of creative iOS applications that celebrate imperfection, analog aesthetics, and mindful digital experiences. Each app is designed to transform everyday moments into something unique and meaningful.

## Apps

### 📷 [Horika](apps/horika/)
**A pocket film ritual — a toy camera's randomness and imperfect beauty in every shot.**

A film simulation camera app that recreates the tactile experience of shooting with a plastic toy camera. Every shot may bring light leaks, grain, color shifts, or blur — these are features, not bugs. Horika embraces the unpredictability and character of analog photography.

**Features:**
- Gallery with sample photos
- Card-based navigation (Botan, Chi, Hoho)
- Film-like unpredictability and character

### 🔐 [Hamster](apps/hamster/)
**Simple, reliable two-factor authenticator (TOTP) to keep your accounts secure.**

A straightforward TOTP authenticator that prioritizes simplicity and reliability for secure account management.

### 📍 [Locter](apps/locter/)
**Automatic location tracking with strong on-device privacy and seamless background operation.**

Privacy-focused location tracking that works automatically in the background while keeping your data secure on your device.

### ☀️ [Purple](apps/purple/)
**Real-time UV index updates with intuitive visual alerts and a purple-themed design.**

Stay protected with real-time UV index monitoring, featuring visual alerts and a distinctive purple aesthetic.

### 📸 [Narda](apps/narda/)
**Two snaps, one story — unexpected juxtapositions and tiny surprises.**

Create meaningful stories through the combination of two photos, discovering unexpected connections and narratives.

### 🎞️ [Perfora](apps/perfora/)
**Add sprocket holes and film frames to photos for a vintage, analog look.**

Transform your digital photos with authentic-looking sprocket holes and film frames for a classic analog aesthetic.

### 📝 [Komore](apps/komore/)
**Writing a poem for you — create poems from your photos, capturing the interplay of light and feeling.**

An AI-powered app that transforms your photos into poetry. Select multiple photos, choose a theme, style, language, and length, and let the app compose a unique poem that captures your visual story.

**Features:**
- Multi-language support
- Multiple theme and style options
- Customizable poem length

### 🪟 [Outside](apps/outside/)
**View from window, story within — create collages of your unique window view while discovering your inner world.**

Document and create collages from your window views, exploring both the external landscape and your internal perspective.

## Project Structure

```
omitlens.com/
├── CNAME                    # Domain configuration
├── index.html              # Main landing page
├── style.css               # Global styles
└── apps/                   # Individual app pages
    ├── hamster/
    ├── horika/
    │   ├── cards/          # Card-based content
    │   └── gallery/        # Photo gallery with 44+ images
    ├── komore/
    ├── locter/
    ├── narda/
    ├── outside/
    ├── perfora/
    └── purple/
```

Each app folder contains:
- `index.html` - App landing page
- `privacy.html` - Privacy policy
- `style.css` - App-specific styles
- `images/` - App icons and screenshots

## Development

This is a static website hosted on GitHub Pages. To view locally:

1. Clone the repository
2. Open `index.html` in a web browser, or
3. Serve with a local web server:
   ```bash
   python -g http.server 8000
   # or
   npx serve
   ```

## Technologies

- HTML5
- CSS3
- Static site hosting (GitHub Pages)
- AVIF image format for optimized performance

## Creator

**Jun Lin** - [linjun.me](https://linjun.me)

## License

All rights reserved. Individual app licenses may vary.

---

*Embracing imperfection and the blurred boundaries between things.*
