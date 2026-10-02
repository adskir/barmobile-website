# Bar Mobile — barmobile.it

Landing page statica (HTML/CSS/JS in un unico file, nessuna build necessaria).

## Struttura
- `index.html` — tutta la landing. La drink list (card con ricetta) è generata da JS: array `DRINKS` + funzione `glassSVG()` che disegna i bicchieri in SVG (illustrazioni originali, nessuna foto esterna).
- `privacy.html` — informativa GDPR.
- `fonts/` — Playfair Display + DM Sans in self-hosting (nessuna chiamata a Google Fonts).

## Configurazione
In fondo a `index.html`:
- `WHATSAPP_NUMBER` — numero in formato internazionale senza `+` (es. `393331234567`). Se vuoto, i pulsanti WhatsApp restano nascosti.
- `FORMSPREE` — endpoint del modulo preventivo (account ClickBari).

## Aggiungere un drink
Aggiungi un oggetto a `DRINKS`: `cat` (spritz | classici | shot | analcolici), `name`, `tag`, `glass` (wine | coupe | martini | highball | rocks | shot), colori `c1`/`c2` oppure `stops` per strati, `ice`, `bubbles`, `salt`, `garnish` (orange, lemon, lime, grapefruit, mint, cherry, beans, cucumber, straw, berries, peel), `ingr`, `method`, `chips`.

## Deploy
Repository collegato a OVH tramite la funzione Git integrata dell'hosting, branch `main`. Ogni push su `main` viene sincronizzato automaticamente su barmobile.it tramite webhook.
