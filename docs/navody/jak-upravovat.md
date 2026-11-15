# Jak upravovat dokumentaci

Každá stránka je obyčejný soubor `.md` (Markdown) ve složce `docs/`.

## Nejrychleji – přímo na webu
1. Na stránce klikni na ikonu :material-file-edit-outline: (vpravo nahoře).
2. Otevře se editor na GitHubu, uprav text a dej **Commit changes**.
3. Za 1–2 minuty je změna na webu.

## Nová stránka
1. Vytvoř soubor ve správné složce, např. `docs/infrastruktura/tiskarna.md`.
2. Přidej ho do `nav:` v souboru `mkdocs.yml`.

## Rozhodovací strom („Co dělat, když…“)
Každý **krok = jedna stránka** ve složce `docs/co-delat-kdyz/`.
Stránka obsahuje otázku nebo postup a tlačítka na další kroky:

```markdown
# Svítí kontrolka?

[Ano](dalsi-krok.md){ .md-button .md-button--primary }
[Ne](jiny-krok.md){ .md-button }
```

Slepé konce vedou na `vyreseno.md` nebo `eskalace.md`.

## Užitečné prvky

```markdown
!!! warning "Pozor"
    Text varování.

??? info "Rozbal pro detail"
    Skrytý text.

- [ ] položka checklistu
```

## Lokální náhled
```bash
pip install -r requirements.txt
mkdocs serve
```
Pak otevři <http://127.0.0.1:8000>.

!!! danger "Hesla nikdy do dokumentace"
    Repozitář/web může být veřejný. Uváděj jen, *kde* hesla najít.
