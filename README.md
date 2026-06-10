# Heemu — Site folder

Everything in this folder, pushed to Vercel, becomes the live site.

## 📁 Folder structure

```
heemu-site/
├── index.html              ← The whole landing page. Edit this for any text changes.
├── images/
│   ├── hero.jpg            ← REQUIRED — your composited hero image
│   ├── demo-poster.jpg     ← REQUIRED — first frame of the demo video (fallback)
│   └── founder.jpg         ← OPTIONAL — photo for founder story section
└── videos/
    └── heemu-setup.mp4     ← REQUIRED — the 3-step setup demo video
```

## 🖼️ Image specs

### `images/hero.jpg` (CRITICAL)
- **What:** Your Gemini hero image with the ayah composited onto the phone
- **Recommended dimensions:** 2160 × 1080 px (2:1 aspect ratio) or whatever Gemini exported
- **Format:** JPG, optimized to <500KB
- **Goes on:** The very top of the page, below the hero headline

### `videos/heemu-setup.mp4` (CRITICAL)
- **What:** Screen recording of you setting up the app and seeing the first intervention
- **Recommended dimensions:** 1080 × 2400 px (portrait, phone aspect ratio)
- **Length:** 8-15 seconds, looping
- **Format:** MP4, H.264, <5MB
- **Goes on:** "How It Works" section, between the headline and the 3 step cards

### `images/demo-poster.jpg` (CRITICAL — pair with video)
- **What:** A still frame from your demo video — shows while video loads
- **Recommended dimensions:** Same as the video (1080 × 2400)
- **Format:** JPG, <200KB
- **How to make:** Screenshot the first frame of your video, save as JPG

### `images/founder.jpg` (OPTIONAL)
- **What:** A real photo for the founder story section. Options:
  - Your hand and Heemu's hand together
  - A backlit silhouette of you holding your phone with Heemu nearby
  - A simple photo of your living room with the phone on the table
  - Any candid moment that ties to the story
- **Recommended dimensions:** 1200 × 1200 px (square) or 1200 × 900 (4:3)
- **Format:** JPG, <300KB
- **Goes on:** Founder Story section (currently commented out in HTML — uncomment when ready)

## ✅ Pre-launch checklist

Before running `vercel`, make sure:

- [ ] `images/hero.jpg` exists (your composited hero)
- [ ] `videos/heemu-setup.mp4` exists (your setup demo)
- [ ] `images/demo-poster.jpg` exists (first frame of video)
- [ ] All `href="#"` and `href="#download"` links in index.html point to real URLs (App Store, Play Store, or waitlist signup)
- [ ] You've previewed the file locally (just open `index.html` in a browser)

## 🚀 Deploy

From inside this folder:

```bash
vercel
```

First time only:
```bash
npm install -g vercel
vercel login
```

## ✏️ Editing later

Everything is in `index.html`. Open it in any text editor. Use Ctrl+F to find what you want to change. Save. Run `vercel --prod` to redeploy.

## 🎨 If a section feels wrong

The Heemu brand colors are defined at the very top of the `<style>` block in `index.html`, as CSS variables:

```css
--cream: #F5EFE4;
--ink: #1A2F26;
--olive: #4A5D3F;
--gold: #B8924A;
```

Change any of these once and every section using that color updates everywhere.
