# 🪔 Festival Wishes — WhatsApp Viral Greeting Website

A lightweight, mobile-first festival greeting website designed for Indian WhatsApp users.
No backend. No database. Pure static HTML. Deploy to Vercel in one click.

---

## 🚀 Deploy to Vercel

1. Upload this folder to GitHub (or drag-drop to Vercel directly)
2. Connect to Vercel → **Deploy**
3. Done! Your site is live.

---

## 🎨 Change Festival (edit 5 lines in `index.html`)

Open `index.html` and find this block near the top `<head>`:

```html
<script>
  const FESTIVAL_NAME    = "Diwali";
  const FESTIVAL_EMOJI   = "🪔";
  const FESTIVAL_SUB     = "Festival of Lights";
  const FESTIVAL_MESSAGE = "wishes you and your family a very Happy Diwali! May this Diwali bring joy, prosperity, and light into your life.";
  const THEME = {
    primary:   "#FF6B00",
    secondary: "#FFB800",
    accent:    "#FF3D00",
    bg:        "#1A0A00",
    card:      "#2D1500",
    light:     "#FFF4E0",
  };
</script>
```

### Festival presets:

| Festival          | FESTIVAL_NAME     | FESTIVAL_EMOJI | primary  | secondary | bg       |
|-------------------|-------------------|----------------|----------|-----------|----------|
| Diwali            | Diwali            | 🪔             | #FF6B00  | #FFB800   | #1A0A00  |
| Holi              | Holi              | 🎨             | #E91E8C  | #FF9800   | #1A0020  |
| Eid               | Eid               | 🌙             | #00897B  | #FFD600   | #001A14  |
| Christmas         | Christmas         | 🎄             | #C62828  | #FFD600   | #001A00  |
| New Year          | New Year          | 🎆             | #1565C0  | #FFD600   | #000A1A  |
| Independence Day  | Independence Day  | 🇮🇳            | #FF6B00  | #128807   | #000D00  |
| Raksha Bandhan    | Raksha Bandhan    | 🧡             | #E91E63  | #FF9800   | #1A0010  |
| Janmashtami       | Janmashtami       | 🦚             | #7B1FA2  | #FFD600   | #0D001A  |

---

## 📋 SEO — Update these in `index.html`

1. Replace all `https://your-domain.vercel.app` with your actual domain.
2. Add an `og-image.png` (1200×630px) to the root folder for WhatsApp link previews.

---

## 💰 Ads — Add Google AdSense

Find these two divs in `index.html`:

```html
<div class="ad-top" id="adTop">Advertisement</div>
<div class="ad-bottom" id="adBottom">Advertisement</div>
```

Replace their contents with your AdSense `<ins>` code. The layout is already prepared — ads will never cover the main content.

---

## 📂 File Structure

```
festival-wishes/
├── index.html      ← Entire website (edit festival config here)
├── robots.txt      ← SEO: allow all crawlers
├── sitemap.xml     ← SEO: site map
├── vercel.json     ← Vercel deployment config
└── README.md       ← This file
```

---

## 🔗 How the sharing works

1. Visitor opens site → enters name → clicks **Create My Wishes**
2. Greeting appears → they click **Share on WhatsApp**
3. WhatsApp opens with pre-filled message + link like `/?sender=Rahul`
4. Receiver opens link → sees greeting from Rahul
5. Receiver clicks **Create Your Own Wishes** → enters their name → shares again

The sender's name is encoded in the URL query string. No server or database needed.

---

## ✅ Performance

- Total page size: ~15 KB HTML + ~8 KB fonts (Google Fonts CDN)
- Zero external JS libraries
- Zero images (emojis only)
- Zero videos / GIFs / audio
- Works on 2G connections
- Smooth on low-end Android phones
