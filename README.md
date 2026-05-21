# Nostalgia Phone - Deploy

## Cosa contiene
- `index.html` - l'app (HTML + CSS + JS, tutto inline)
- `sw.js` - service worker per supporto offline
- Manifest e icone sono inline nell'HTML

## Test PWA su iPhone
1. Apri l'URL in Safari (non Chrome - su iOS solo Safari supporta installazione PWA)
2. Tocca il bottone Share (quadrato con freccia)
3. Scorri in basso e tocca "Aggiungi alla schermata Home"
4. Conferma - appare un'icona sull'home screen
5. Da quel momento si apre come app fullscreen, senza barra Safari

## Test PWA su Android
1. Apri l'URL in Chrome
2. Dovrebbe apparire un prompt "Installa app" in basso, oppure menu → "Aggiungi alla schermata Home"

Quando aggiorni `index.html`, **cambia anche `CACHE_NAME` in `sw.js`** (es. da `nostalgia-phone-v1` a `v2`) altrimenti gli utenti vedranno la versione cached vecchia per giorni.
