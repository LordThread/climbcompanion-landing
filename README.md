# climbcompanion-landing

Sito statico pubblico di Climb Companion: landing page, Informativa sulla Privacy e Termini di Servizio (IT/EN), pronto per GitHub Pages.

## File

- `index.html` / `index-en.html` — landing page (IT/EN), tema scuro con i colori dell'icona dell'app
- `privacy-it.html` / `privacy-en.html` — Informativa sulla Privacy
- `terms-it.html` / `terms-en.html` — Termini di Servizio / EULA abbonamento Plus
- `style.css` — stile condiviso da tutte le pagine (header, tipografia, pagine legali)
- `favicon-32.png`, `apple-touch-icon.png`, `icon-512.png` — icona del sito, ricavata dall'icona reale dell'app
- `screen-projects.png`, `screen-training.png`, `screen-sessions.png`, `screen-analytics.png` — screen reali catturati dal Simulatore iOS (italiano), usati in `index.html`
- `screen-projects-en.png`, `screen-training-en.png`, `screen-sessions-en.png`, `screen-analytics-en.png` — stessi screen catturati con il Simulatore in inglese, usati in `index-en.html`

**Nota sugli screen**: sono catture reali dell'app da Simulatore (⌘S), ridimensionate per il web. Se in futuro aggiorni l'app, ricatturale e sostituisci i file mantenendo lo stesso nome (quelli senza suffisso per l'italiano, quelli con `-en` per l'inglese).

## Come pubblicarlo (GitHub Pages, gratis)

1. Vai su [github.com/new](https://github.com/new) e crea un nuovo repository:
   - Nome: `climbcompanion-landing`
   - Visibilità: **Public** (obbligatorio per GitHub Pages gratuito)
   - Non aggiungere README/gitignore/licenza (li abbiamo già)
2. Sul tuo Mac, in una cartella a tua scelta (diversa da `ClimbCompanionV2`):
   ```bash
   git clone https://github.com/<tuo-username>/climbcompanion-landing.git
   ```
3. Copia dentro la cartella appena clonata **tutti** i file di questo pacchetto, mantenendoli alla radice (non in una sottocartella): `index.html`, `index-en.html`, `privacy-it.html`, `privacy-en.html`, `terms-it.html`, `terms-en.html`, `style.css`, `favicon-32.png`, `apple-touch-icon.png`, `icon-512.png`, questo `README.md`.
4. Fai il primo commit e push:
   ```bash
   cd climbcompanion-landing
   git add .
   git commit -m "Sito iniziale: landing, privacy, termini"
   git push
   ```
5. Su GitHub, vai in **Settings ▸ Pages** del repository:
   - Source: `Deploy from a branch`
   - Branch: `main` (o `master`), cartella `/ (root)`
   - Salva
6. Dopo qualche minuto il sito sarà online su:
   ```
   https://<tuo-username>.github.io/climbcompanion-landing/
   ```
   e le pagine legali su `.../privacy-it.html`, `.../terms-it.html`, ecc.

## Quando aggiorni Privacy/Termini

Se il legale chiede modifiche al testo, basta modificare il file `.html` corrispondente, fare `git commit` + `git push`: GitHub Pages aggiorna il sito automaticamente in un minuto o due, nessuna azione extra.

## Se in futuro compri il dominio climbcompanion.com

1. Crea nel repository un file chiamato `CNAME` (senza estensione) con dentro solo:
   ```
   climbcompanion.com
   ```
2. Dal pannello del tuo registrar, aggiungi questi record DNS (i valori esatti sono nella pagina ufficiale di GitHub, "Managing a custom domain for your GitHub Pages site"):
   - un record `A` verso gli IP di GitHub Pages, oppure
   - un record `CNAME` verso `<tuo-username>.github.io` se usi un sottodominio come `www.climbcompanion.com`
3. In **Settings ▸ Pages** del repo, inserisci il dominio personalizzato e attiva "Enforce HTTPS".

Il sito resta lo stesso, cambia solo l'indirizzo con cui è raggiungibile.
