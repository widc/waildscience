# 🎉 wAIld Science Web - Kompletní balíček

Gratuluji! Máte připravené kompletní webové stránky pro wAIld Science.

## 📦 Co je v balíčku?

### Hlavní soubory
- **index.html** - Hlavní stránka webu
- **catalog.html** - Stránka s katalogem prací
- **style.css** - Všechny styly (310+ řádků)
- **script.js** - JavaScript pro interaktivitu
- **favicon.svg** - Ikona webu (AI logo)

### Konfigurace
- **CNAME** - Nastavení vlastní domény
- **LICENSE** - MIT pro kód, CC BY 4.0 pro obsah
- **.gitignore** - Git ignorované soubory

### Dokumentace
- **README.md** - Kompletní dokumentace projektu
- **DEPLOYMENT.md** - Podrobný návod na nasazení
- **CATALOG_TEMPLATE.md** - Šablona pro přidávání prací

## 🎨 Design

### Barevné schéma
- **Primární fialová**: #a855f7 (AI písmena)
- **Primární zelená**: #10b981 (text)
- **Tmavé pozadí**: #0f172a (hlavní)
- **Tmavé pozadí 2**: #1e293b (sekce)

### Features
✅ Moderní, čistý design  
✅ Plně responzivní (mobil, tablet, desktop)  
✅ Smooth scrolling  
✅ Animace při scrollování  
✅ Optimalizováno pro rychlost  
✅ SEO friendly  
✅ Accessibility considerations  

## 🚀 Jak začít?

### Varianta A: GitHub Desktop (nejjednodušší)

1. **Stáhněte všechny soubory**
2. **Otevřete GitHub Desktop**
3. File → Add Local Repository
4. Vyberte složku s weby
5. Publish repository → `widc/waildscience`
6. Jděte na GitHub.com/widc/waildscience/settings/pages
7. Aktivujte GitHub Pages (Branch: main, root)
8. ✅ Hotovo!

### Varianta B: Git příkazová řádka

```bash
cd /cesta/ke/staženým/souborům
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/widc/waildscience.git
git push -u origin main
```

Pak aktivujte GitHub Pages v nastavení repozitáře.

### Varianta C: Přímý upload na GitHub

1. Jděte na https://github.com/widc/waildscience
2. Klikněte "Add file" → "Upload files"
3. Přetáhněte všechny soubory
4. Commit changes
5. Aktivujte GitHub Pages

## 🌐 Nastavení domény

**Po aktivaci GitHub Pages:**

1. **U registrátora domény** (wedos.cz, forpsi.com, ...):
   - Přidejte 4 A záznamy (viz DEPLOYMENT.md)
   - Přidejte CNAME záznam pro www

2. **Na GitHubu**:
   - Settings → Pages → Custom domain: `waildscience.org`
   - Zaškrtněte "Enforce HTTPS" (až bude dostupné)

**DNS propagace trvá 24-48 hodin!**

## 📝 Jak přidávat práce do katalogu?

1. Otevřete `catalog.html`
2. Najděte zakomentovanou šablonu
3. Zkopírujte ji a vyplňte:
   - Název práce
   - Autor (Rok)
   - Popis (2-3 věty)
   - Odkazy (Dokument, DOI)
4. Commitněte a pushněte

**Detailní návod v souboru CATALOG_TEMPLATE.md**

## 🔧 Úpravy obsahu

### Změna textu
- Editujte `index.html` nebo `catalog.html`
- Obsah je strukturovaný do jasných sekcí
- Každá sekce má komentáře pro orientaci

### Změna barev
- Otevřete `style.css`
- Upravte CSS proměnné na začátku (řádky 2-13)
- Všechny barvy se změní automaticky

### Přidání nové stránky
1. Vytvořte nový .html soubor
2. Zkopírujte strukturu z index.html nebo catalog.html
3. Přidejte odkaz do navigace

## 📊 Struktura webu

```
index.html
├── Hero sekce (úvodní banner)
├── O konceptu (co je wAIld Science)
├── Kritéria (kdo může přispět)
├── Jak se zúčastnit (proces)
└── Kontakt

catalog.html
└── Seznam prací (zatím prázdný)
```

## ✅ Checklist před spuštěním

- [ ] Zkontrolujte, že všechny soubory jsou v repozitáři
- [ ] Otestujte web lokálně (otevřete index.html v prohlížeči)
- [ ] Zkontrolujte odkazy v navigaci
- [ ] Ověřte kontaktní informace
- [ ] Aktivujte GitHub Pages
- [ ] Nastavte DNS (pokud používáte vlastní doménu)
- [ ] Po publikaci founding dokumentu: aktualizujte DOI link

## 🎯 Co dál?

1. **Publikujte founding dokument** na Figshare
2. **Aktualizujte DOI** v index.html (sekce Contact)
3. **Čekejte na první žádosti** o zařazení
4. **Přidávejte práce** do katalogu

## 🆘 Podpora

### Problémy s nasazením?
Viz **DEPLOYMENT.md** - kompletní troubleshooting guide

### Problémy s HTML/CSS?
- Validujte HTML: https://validator.w3.org/
- Validujte CSS: https://jigsaw.w3.org/css-validator/

### Dotazy k projektu?
info@waildscience.org

## 🎨 Inspirace pro budoucí rozšíření

- **Blog sekce** - články o wAIld Science
- **Statistiky** - kolik prací, autorů, oborů
- **Vyhledávání** - v katalogu
- **Tagy** - kategorizace prací
- **RSS feed** - pro nové práce
- **Newsletter** - pro zájemce

---

## 🚀 Teď je čas to spustit!

Web je připravený. Stačí nahrát na GitHub, aktivovat Pages, a můžete začít.

**Hodně štěstí s projektem wAIld Science!** 🌟