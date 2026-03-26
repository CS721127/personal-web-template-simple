# Personal Website Template

> **Based on the design by [cs721127](https://github.com/CS721127)** — deep-blue & gold literary theme.  
> This template preserves the full UI, layout, and features while replacing all personal information with clearly-marked placeholders.

---

## Quick Start

1. **Fork this repo** to a new repository (or the root of `yourusername.github.io`).
2. **Find every `<!-- TODO: ... -->`** comment in the HTML files — that's every piece of content you need to replace.
3. **Replace placeholder images** — swap `asset/images/placeholder.svg` src attributes with your own photo paths, or drop your images into `asset/images/`.
4. **Push to GitHub Pages** — you're live.

---

## Folder Structure

```
template/
├── index.html                  ← Home page
├── README.md                   ← This file
├── asset/
│   ├── css/
│   │   ├── theme.css           ← Shared colors, fonts, header, nav, footer
│   │   ├── pages.css           ← Shared page-level components (cards, hero, etc.)
│   │   ├── article.css         ← Blog post article layout
│   │   └── audio.css           ← Audio player styles (if you use audio posts)
│   ├── js/
│   │   └── audio.js            ← Audio player logic
│   └── images/
│       └── placeholder.svg     ← Generic image placeholder — replace with your photos
├── about/
│   ├── index.html              ← About page (profile, timeline, skills)
│   └── intro/
│       ├── index.html          ← Interactive "24-hour day" intro page
│       ├── style.css           ← Intro page styles (self-contained)
│       └── script.js           ← Intro page JS (clock, gallery, fun facts)
├── blog/
│   ├── index.html              ← Blog index (filter + search)
│   └── sample-post.html        ← Template for a single blog post
├── professional/
│   └── index.html              ← Professional CV-style page
├── projects/
│   └── index.html              ← Projects showcase
└── contact/
    └── index.html              ← Contact page (email, socials, friend links)
```

---

## Customising Each Page

### 🏠 Home (`index.html`)
- Replace name, tagline, hero photo, and bio in the `.hero` section.
- Replace the 3 featured post cards with your actual posts.
- Replace the greeting section text and signature.

### 👤 About (`about/index.html`)
- Replace profile photo, bio, interest tags.
- Edit the `Academic Journey` timeline: duplicate `<li class="timeline-item">` blocks for each institution.
- Edit the `Skills` grid.

### 🎬 Interactive Intro (`about/intro/index.html`)
- Replace name, profile photo, bio, education timeline.
- Replace tech stack tags, experience cards, fun chaotic bullets.
- **Gallery**: drop your travel photos into the `about/intro/` folder, then update the `background-image: url(...)` values on each `.gallery-item`.
- **Fun Facts**: open `about/intro/script.js` and update the `funFacts` array with your own facts.

### 📝 Blog Index (`blog/index.html`)

#### Adding a new post — 3 steps:
1. **Duplicate** `blog/sample-post.html` → `blog/your-post-slug.html`.
2. **Fill in** the title, date, body content, and images.
3. **Duplicate a card** in `blog/index.html` and update its `data-tags`, image, title, date, description, and `href`.

The filter and search update automatically — no other changes needed.

#### Adding a new filter tag:
- Add a `<button class="filter-option" data-tag="your-tag">Label</button>` in the filter bar.
- Set `data-tags="your-tag"` on the matching blog card.

### 💼 Professional (`professional/index.html`)
- Duplicate `.experience-item` blocks inside each `.professional-card` to add more entries.
- Delete cards you don't need (e.g. a "Research" card if you don't have any).

### 🚀 Projects (`projects/index.html`)
- Duplicate `<article class="blog-entry">` blocks for each project.
- Update the link text and `href` (use `"In Progress…"` if the project isn't published yet).

### 📬 Contact (`contact/index.html`)
- Replace email, GitHub, LinkedIn, Instagram URLs.
- Add or remove `.social-btn` links as needed.
- Delete the "Friend Links" card if you don't have any external links to share.

---

## CSS Customisation

All color tokens are defined at the top of `asset/css/theme.css` in the `:root` block:

```css
--ocean: #1a3a5c;       /* Primary dark blue */
--gold:  #8a6a28;       /* Accent gold */
--parchment: #f4f7fb;   /* Page background */
/* ... and more */
```

Change these values to completely re-skin the site without touching any other CSS.

---

## Attribution

This template was designed and built by **[cs721127](https://github.com/CS721127)**.  
Please keep the attribution line in the footer of each page:
```html
Template by <a href="https://github.com/CS721127">cs721127</a>
```

---

*Happy writing! — cs721127*
