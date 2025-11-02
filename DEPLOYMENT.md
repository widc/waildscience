# Deployment Guide - wAIld Science Web

## Rychlý start (5 minut)

### 1. Upload na GitHub

```bash
# Ve vašem lokálním adresáři
git init
git add .
git commit -m "Initial commit: wAIld Science website"
git branch -M main
git remote add origin https://github.com/widc/waildscience.git
git push -u origin main
```

### 2. Aktivace GitHub Pages

1. Jděte na: https://github.com/widc/waildscience/settings/pages
2. **Source**: Deploy from a branch
3. **Branch**: `main` / folder: `/ (root)`
4. Klikněte **Save**

✅ Web bude dostupný za 1-2 minuty na: `https://widc.github.io/waildscience/`

---

## Nastavení vlastní domény (waildscience.org)

### Krok 1: DNS u registrátora

U vašeho registrátora domény (např. wedos.cz) nastavte:

**A záznamy** (apex domain):
```
Typ: A
Název: @
Hodnota: 185.199.108.153

Typ: A
Název: @
Hodnota: 185.199.109.153

Typ: A
Název: @
Hodnota: 185.199.110.153

Typ: A
Název: @
Hodnota: 185.199.111.153
```

**CNAME záznam** (www subdomain):
```
Typ: CNAME
Název: www
Hodnota: widc.github.io
```

### Krok 2: GitHub Pages nastavení

1. Jděte na: https://github.com/widc/waildscience/settings/pages
2. **Custom domain**: `waildscience.org`
3. Klikněte **Save**
4. Počkejte na DNS check (může trvat 24-48 hodin)
5. Zaškrtněte **Enforce HTTPS** (až bude dostupné)

### Krok 3: CNAME soubor

Soubor `CNAME` už je v repozitáři s obsahem:
```
waildscience.org
```

Pokud by byl smazán, vytvořte ho znovu.

---

## Ověření

### Test DNS propagace

```bash
# Zkontrolujte A záznamy
dig waildscience.org +short

# Mělo by vrátit:
# 185.199.108.153
# 185.199.109.153
# 185.199.110.153
# 185.199.111.153

# Zkontrolujte CNAME
dig www.waildscience.org +short

# Mělo by vrátit:
# widc.github.io
```

### Online nástroje

- https://www.whatsmydns.net/ (globální propagace)
- https://dnschecker.org/ (DNS checker)

---

## Aktualizace obsahu

### Běžné změny

```bash
# Upravte soubory (index.html, catalog.html, atd.)
git add .
git commit -m "Update: popis změny"
git push
```

Změny se projeví na webu do 1-2 minut.

### Přidání práce do katalogu

Viz soubor `CATALOG_TEMPLATE.md` pro detaily.

```bash
# 1. Upravte catalog.html
# 2. Commit
git add catalog.html
git commit -m "Add: Název práce - Autor"
git push
```

---

## Časté problémy

### Web se nezobrazuje

1. Zkontrolujte GitHub Actions: https://github.com/widc/waildscience/actions
2. Chyby v HTML/CSS? Validujte: https://validator.w3.org/
3. Počkejte 2-3 minuty na build

### Doména nefunguje

1. DNS propagace trvá 24-48 hodin
2. Zkontrolujte DNS záznamy u registrátora
3. Vyčistěte browser cache (Ctrl+Shift+R)
4. Zkuste inkognito režim

### HTTPS certifikát chybí

1. DNS musí být správně nastaveno
2. V Settings → Pages: odškrtněte a znovu zaškrtněte "Enforce HTTPS"
3. Počkejte 15-30 minut
4. Let's Encrypt certifikát se vytvoří automaticky

---

## Maintenance

### Pravidelné úkoly

- Aktualizace katalogu (podle příchozích žádostí)
- Kontrola fungování odkazů
- Backup repozitáře (GitHub už je backup, ale můžete mít lokální)

### Monitoring

- GitHub poskytuje analytics v Insights → Traffic
- Případně přidejte Google Analytics (volitelné)

---

## Kontakt pro podporu

Pokud máte problémy s deploymentem:

1. Zkontrolujte GitHub Pages dokumentaci: https://docs.github.com/pages
2. Kontaktujte: info@waildscience.org