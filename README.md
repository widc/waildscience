# wAIld Science - Web Pages

Webové stránky pro [waildscience.org](https://waildscience.org)

## O projektu

wAIld Science je koncept označující průkopnický vědecký výzkum, který stojí mezi přísně akademickou vědou a science fiction. Prostor pro samostatné badatele, kteří zkoumají odvážné hypotézy bez institucionálního zázemí.

## Struktura projektu

```
waildscience/
├── index.html          # Hlavní stránka
├── catalog.html        # Katalog prací
├── style.css           # Styly
├── script.js           # JavaScript
└── README.md           # Tento soubor
```

## Technologie

- Statický HTML/CSS/JavaScript
- Žádné závislosti, frameworky ani build proces
- Responzivní design
- Optimalizováno pro GitHub Pages

## Lokální vývoj

1. Naklonujte repozitář:
```bash
git clone https://github.com/widc/waildscience.git
cd waildscience
```

2. Otevřete `index.html` v prohlížeči nebo použijte lokální server:
```bash
# Python 3
python -m http.server 8000

# Node.js
npx serve

# VS Code Live Server extension
```

3. Navštivte `http://localhost:8000`

## Deployment na GitHub Pages

1. V repozitáři jděte do Settings → Pages
2. Source: Deploy from a branch
3. Branch: `main` / `root`
4. Save

Stránky budou dostupné na: `https://widc.github.io/waildscience/`

### Vlastní doména (waildscience.org)

1. V repozitáři vytvořte soubor `CNAME` s obsahem:
```
waildscience.org
```

2. U registrátora domény nastavte DNS:
```
A record    @    185.199.108.153
A record    @    185.199.109.153
A record    @    185.199.110.153
A record    @    185.199.111.153
CNAME       www  widc.github.io
```

3. V Settings → Pages → Custom domain zadejte: `waildscience.org`
4. Zaškrtněte "Enforce HTTPS"

## Jak přidat práci do katalogu

1. Otevřete `catalog.html`
2. Odkomentujte template v sekci catalog-grid
3. Přidejte novou položku:

```html
<div class="catalog-item">
    <h3>Název práce</h3>
    <p class="author">Jméno Autora (2025)</p>
    <p class="description">
        Stručný popis obsahu a přínosu práce (2-3 věty).
    </p>
    <div class="links">
        <a href="URL_K_DOKUMENTU" target="_blank">📄 Dokument</a>
        <a href="DOI_URL" target="_blank">🔗 DOI</a>
    </div>
</div>
```

4. Commitněte a pushněte změny

## Úprava obsahu

### Změna textu
Editujte přímo `index.html` - obsah je strukturovaný do jasných sekcí.

### Změna barev
V `style.css` upravte CSS proměnné na začátku:

```css
:root {
    --primary-purple: #a855f7;
    --primary-green: #10b981;
    --dark-bg: #0f172a;
    /* ... */
}
```

### Přidání nové sekce
1. Přidejte HTML sekci do `index.html`
2. Přidejte odkaz do navigace
3. Případně přidejte specifické styly do `style.css`


## Licence

Obsah: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)  
Kód: MIT License

## Kontakt

- E-mail: info@waildscience.org
- Autor: Vít Koksa ([ORCID](https://orcid.org/0009-0000-1796-5683))
- GitHub: [github.com/widc/waildscience](https://github.com/widc/waildscience)

---


Doména registrována do roku 2030
