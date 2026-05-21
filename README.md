# Nostalgia Phone

Web app vintage del telefono FATME a disco. Installabile come PWA su iPhone e Android.

## File del progetto

- `index.html` - l'app
- `sw.js` - service worker (offline)
- `manifest.json` - PWA manifest
- `icon-192.png`, `icon-512.png` - icone PWA
- `icon-512-maskable.png` - icona maskable per Android
- `apple-touch-icon.png` - icona per iOS home screen

**Tutti i file devono stare nella stessa cartella, nel root del sito.**

## Deploy su GitHub Pages

```bash
git add .
git commit -m "PWA: manifest + icone esterne"
git push
```

Aspetta 30-60 secondi, ricarica https://pasfranc.github.io/nostalgia-phone/

## Come installare l'app

### Android (Chrome)
1. Apri il sito in Chrome
2. Dopo qualche secondo appare un prompt in basso: "Aggiungi a schermata Home"
3. Se non appare: menu ⋮ -> "Aggiungi a schermata Home" / "Installa app"

### iPhone (Safari)
Non esiste prompt automatico, Apple non lo permette. Devi:
1. Apri in **Safari** (non Chrome)
2. Tocca Share (quadrato con freccia in basso)
3. Scorri giù -> "Aggiungi alla schermata Home"
4. Conferma

### Desktop (Chrome, Edge)
- Icona + nella barra URL, oppure menu -> "Installa Nostalgia Phone"

## Aggiornamenti

Quando modifichi index.html:
1. Cambia anche CACHE_NAME in sw.js (es. v4 -> v5)
2. Commit + push

Senza bump del cache name gli utenti vedono la versione vecchia per giorni.

## Note

- Audio: serve interruttore Silent OFF su iPhone
- Chiamata: il bottone verde apre tel:numero, il sistema chiede conferma
- Prefisso internazionale: usa 00 (es. 0049 per Germania)
