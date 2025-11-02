# Template pro přidání práce do katalogu

Tento soubor slouží jako reference pro přidávání nových prací do `catalog.html`.

## Postup

1. Otevřete `catalog.html`
2. Najděte sekci s komentářem `<!-- Template for future catalog items -->`
3. Odkomentujte `<div class="catalog-grid">` pokud je první položka
4. Přidejte novou položku podle šablony níže

## Šablona

```html
<div class="catalog-item">
    <h3>Název práce</h3>
    <p class="author">Jméno Autora (Rok)</p>
    <p class="description">
        Stručný popis obsahu a přínosu práce. 2-3 věty vysvětlující, 
        o čem práce je a proč je zajímavá. Tento text by měl být 
        informativní, ale stručný.
    </p>
    <div class="links">
        <a href="https://doi.org/10.XXXX/XXXX" target="_blank">📄 Dokument</a>
        <a href="https://doi.org/10.XXXX/XXXX" target="_blank">🔗 DOI</a>
    </div>
</div>
```

## Příklad

```html
<div class="catalog-item">
    <h3>Formalizace memetiky pomocí teorie kategorií</h3>
    <p class="author">Vít Koksa (2025)</p>
    <p class="description">
        Průkopnický pokus o formalizaci memetiky využitím nástrojů 
        teorie kategorií. Propojuje objektově orientované programování, 
        sémiotiku a evoluční biologii v jednotném rámci.
    </p>
    <div class="links">
        <a href="https://figshare.com/articles/..." target="_blank">📄 Dokument</a>
        <a href="https://doi.org/10.6084/m9.figshare..." target="_blank">🔗 DOI</a>
    </div>
</div>
```

## Poznámky

- Pokud práce nemá DOI, můžete dát pouze odkaz na dokument
- Popis by měl být 2-3 věty (max ~150 slov)
- Použijte příjmení a jméno autora
- Rok publikace v závorkách
- Ujistěte se, že všechny odkazy fungují (target="_blank" otevře v nové záložce)

## Po přidání

1. Commitněte změny: `git add catalog.html`
2. `git commit -m "Add: [Název práce]"`
3. `git push origin main`
4. Změny se projeví na webu do několika minut