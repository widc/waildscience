# 🌍 Bilingual Website Structure

The wAIld Science website is now bilingual (Czech/English).

## 📁 Structure

```
waildscience/
├── index.html          # Czech homepage
├── catalog.html        # Czech catalog
├── style.css           # Shared styles
├── script.js           # Shared JavaScript
├── favicon.svg         # Favicon
└── en/                 # English version
    ├── index.html      # English homepage
    └── catalog.html    # English catalog
```

## 🔗 URLs

- **Czech (default)**: `waildscience.org/`
- **English**: `waildscience.org/en/`

## 🌐 Language Switcher

Both versions have a language switcher in the navigation:
- Czech pages: `🌐 EN` → links to `/en/`
- English pages: `🌐 CZ` → links to `/`

## 🎨 Shared Resources

CSS, JavaScript, and favicon are shared between both versions:
- `../style.css`
- `../script.js`
- `../favicon.svg`

This means:
- ✅ One place to update styles
- ✅ Consistent design across languages
- ✅ Easier maintenance

## 📝 Adding Content

### Adding to Czech catalog:
Edit `/catalog.html`

### Adding to English catalog:
Edit `/en/catalog.html`

**Remember to add the same work to both catalogs!**

### Translating titles:
Keep the original language titles for works, add English description:

```html
<h3>Original Czech Title</h3>
<p class="description">
    English description of the work...
</p>
```

## 🔄 Keeping Both Versions in Sync

When you update content, remember to update both:
1. Czech version (`/index.html`, `/catalog.html`)
2. English version (`/en/index.html`, `/en/catalog.html`)

## 🚀 Deployment

No special configuration needed for GitHub Pages. The `/en/` folder will work automatically.

After pushing to GitHub:
- `waildscience.org/` → Czech
- `waildscience.org/en/` → English

### Work Titles in Catalog

Currently, work titles link to Czech documents. When English versions become available:
1. Add note in description: "(Czech document, English version available)"
2. Or create separate entries for different language versions

## 🆘 Troubleshooting

### Links not working in `/en/`?
Check that relative paths use `../`:
- `<link rel="stylesheet" href="../style.css">`
- `<script src="../script.js"></script>`
- `<a href="../index.html">`

### Language switcher not styled?
Make sure `style.css` includes:
```css
nav a.lang-switch {
    color: var(--primary-purple);
    /* ... */
}
```
