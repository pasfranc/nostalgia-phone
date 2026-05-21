# Nostalgia Phone — Deploy

## Cosa contiene
- `index.html` — l'app (HTML + CSS + JS, tutto inline)
- `sw.js` — service worker per supporto offline
- Manifest e icone sono inline nell'HTML

## Deploy su Netlify (più veloce, gratis, 2 minuti)

1. Vai su https://app.netlify.com/drop (anche senza account)
2. Trascina la cartella che contiene `index.html` e `sw.js` (NON solo i file singoli — proprio la cartella)
3. Netlify ti dà un URL tipo `https://random-name-12345.netlify.app`
4. Da "Site settings" → "Change site name" puoi cambiarlo in `nostalgiaphone` se è libero, sennò aggiungi un suffisso come `nostalgia-phone-pako`

L'HTTPS è automatico, le PWA possono essere installate.

## Test PWA su iPhone
1. Apri l'URL in Safari (non Chrome — su iOS solo Safari supporta installazione PWA)
2. Tocca il bottone Share (quadrato con freccia)
3. Scorri in basso e tocca "Aggiungi alla schermata Home"
4. Conferma — appare un'icona sull'home screen
5. Da quel momento si apre come app fullscreen, senza barra Safari

## Test PWA su Android
1. Apri l'URL in Chrome
2. Dovrebbe apparire un prompt "Installa app" in basso, oppure menu → "Aggiungi alla schermata Home"

## Modifiche future
Per aggiornare l'app dopo il deploy: ri-trascina la cartella su Netlify Drop (stesso sito), oppure collega un repo GitHub al sito per auto-deploy.

Quando aggiorni `index.html`, **cambia anche `CACHE_NAME` in `sw.js`** (es. da `nostalgia-phone-v1` a `v2`) altrimenti gli utenti vedranno la versione cached vecchia per giorni.
