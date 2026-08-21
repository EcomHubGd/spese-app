# Spese — app di gestione spese personali

## Come installarla su iPhone

L'app è un file HTML che gira offline, ma per usare "Aggiungi a Home" con icona
e funzionamento offline vero (service worker) serve che sia servita via https.
Il modo più veloce e gratuito è GitHub Pages:

1. Crea un repo GitHub (anche privato) e carica questi file
   (index.html, manifest.json, sw.js, cartella icons/)
2. Settings → Pages → Deploy from branch → main → salva
3. Apri il link che ti dà GitHub Pages (tipo tuonome.github.io/spese) su Safari da iPhone
4. Tocca il tasto Condividi → "Aggiungi alla schermata Home"
5. Fatto: hai l'icona come un'app vera, si apre a schermo intero, funziona offline

## In alternativa (zero setup, solo per provarla subito)

Apri direttamente index.html in Safari su iPhone (es. da Mail, iCloud Drive o AirDrop).
Funziona comunque, puoi anche fare "Aggiungi alla Home", ma senza hosting https
il service worker offline non si attiva (comunque l'app non fa mai chiamate di rete,
quindi funziona offline lo stesso).

## Dati

Tutto è salvato solo sul tuo telefono (localStorage del browser). Nessun server,
nessun account, nessun dato che esce dal dispositivo. Se cancelli i dati di Safari
per quel sito, perdi lo storico — se vuoi in futuro aggiungo un export/import JSON
per fare backup.
