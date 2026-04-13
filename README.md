# South Coast Hospitality — Website

Two café venues on the NSW South Coast, hosted in one GitHub repository.

## Structure

```
/
├── index.html              ← Group landing page (venue selector)
├── three66/
│   └── index.html          ← Three66 Espresso Bar, Lilli Pilli
└── crumb/
    └── index.html          ← Crumb Cafe, Batehaven
```

## Image files required

Each venue folder should contain its own images. Copy your existing images into the correct subfolder.

### three66/
- `logo.jpg` — Three66 logo
- `view.JPG` — Waterfront/hero shot
- `coffee.jpg`
- `beef-burger.JPG`
- `eggs-benny.JPG`
- `sweet-corn-fritters.JPG`
- `pancakes.JPG`
- `pastry-cabinet.JPG`
- `store-front.JPG`

### crumb/
- `crumb-logo.png` — Crumb logo
- `crumb-vibe.jpg` — Hero/atmosphere shot
- `crumb-coffee.jpg`
- `crumb-pastries.jpg`
- `crumb-toastie.jpg`
- `crumb-smashed-avo.jpg`
- `crumb-br-roll.jpg`
- `crumb-healthy.jpg`
- `crumb-storefront.jpg`

## Deploying to GitHub Pages

1. Push this repo to GitHub
2. Go to Settings → Pages
3. Source: Deploy from a branch → `main` → `/ (root)`
4. The site will be live at `https://yourusername.github.io/repo-name/`

## Google Maps

The embedded maps in the Find Us section use a placeholder API key. Replace `AIzaSyD-9tSrke72PouQMnMX-a7eZSW0jkFMBWY` with your own key from the [Google Cloud Console](https://console.cloud.google.com/), or swap the `<iframe src>` for a standard Google Maps embed URL (no API key required):

```html
<iframe src="https://www.google.com/maps/embed?pb=..." ...></iframe>
```

Get the embed URL from Google Maps → Share → Embed a map.

## Adding menu items

Each menu item in the HTML follows this pattern:

```html
<div class="menu-item" data-cat="CATEGORY">
  <div class="menu-item-img" style="background-image:url('image.jpg')"></div>
  <div class="menu-item-body">
    <span class="menu-item-cat">Category Label</span>
    <h4 class="menu-item-name">Item Name</h4>
    <p class="menu-item-desc">Description text here.</p>
  </div>
</div>
```

Available `data-cat` values:
- **Three66:** `coffee`, `breakfast`, `mains`, `sweets`, `drinks`
- **Crumb:** `coffee`, `baked`, `breakfast`, `light`, `drinks`

To add a new tab category, add a button to `.menu-tabs` and use the matching `data-cat` on items.
