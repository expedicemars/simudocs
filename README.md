# SimuDocs

Dokumentace ostrovní sítě pro simulaci letu na Mars.

Fyzický server s **Proxmoxem**, na kterém běží virtuální stroje:

- **OPNsense** – router a firewall
- **Windows Server** – Active Directory
- **Debian** – aplikační server

Web: <https://expedicemars.github.io/simudocs/>

## Obsah

| Sekce | Složka | Popis |
|---|---|---|
| Zapojení | `docs/zapojeni.md` | Jak server a síťové prvky zapojit a spustit |
| Infrastruktura | `docs/infrastruktura/` | Přehled sítě (diagram) a stránka pro každý stroj |
| Co dělat, když… | `docs/co-delat-kdyz/` | Proklikávací rozhodovací strom pro řešení problémů |
| Pro správce | `docs/navody/` | Jak dokumentaci upravovat |

## Jak upravovat

Nejjednodušší je kliknout na ikonu ✏️ na libovolné stránce webu, upravit text
na GitHubu a dát **Commit changes**. Podrobnosti (nová stránka, nový krok
rozhodovacího stromu) jsou v [docs/navody/jak-upravovat.md](docs/navody/jak-upravovat.md).

> **Hesla nikdy do dokumentace** – uváděj jen, kde je najít.

## Lokální náhled

```bash
pip install -r requirements.txt
mkdocs serve        # náhled na http://127.0.0.1:8000
mkdocs build        # vygeneruje statický web do site/
```

## Nasazení

Každý push na `main` spustí GitHub Actions (`.github/workflows/deploy.yaml`),
který web sestaví a nasadí na GitHub Pages.

## Offline provoz

Ostrovní síť nemusí mít internet, proto web nepoužívá žádné CDN (fonty vypnuté,
Mermaid přibalený v `docs/assets/js/`, plugin `offline`). Složku `site/` lze
hostovat na Debian serveru nebo otevřít přímo z flashky.

Postaveno na [MkDocs](https://www.mkdocs.org) + [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).
