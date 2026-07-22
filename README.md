# makkeroni-web

Sito Astro per makkeroni.com — pronto per GitHub Pages.

## Cosa contiene
- Home, Chi siamo, Prodotti, Contatti in 4 lingue (ES/IT/EN/CA)
- 3 ricette (Carbonara, Cacio e Pepe, Spaghetti alla Nerano) — per ora solo in spagnolo
- Pagine legali (aviso legal, privacy, cookie, accessibilità)
- Workflow GitHub Actions già pronto per build + deploy automatico

## Come caricarlo su GitHub (repository makkeroni-web)

1. Scarica e scompatta questo progetto
2. Nel repository `github.com/Makkeroni/makkeroni-web`, carica **tutto il contenuto** di questa cartella (mantenendo la struttura di cartelle)
   - Su GitHub web: trascina i file/cartelle nella pagina principale del repository ("Add file" → "Upload files")
   - Attenzione: la cartella `.github` (nascosta) deve essere caricata per intero, così come `src`, `public`, e i file alla radice (`package.json`, `astro.config.mjs`, `.gitignore`)
3. Dopo il caricamento, vai su Settings → Pages → Source → **GitHub Actions** (se non l'hai già fatto)
4. Ogni push sul branch `main` farà partire automaticamente la build e la pubblicazione

## Immagini
Le immagini vanno inserite in `public/images/`. Al momento la struttura le referenzia solo per il logo (`/images/logo-makkeroni.png`) — quando hai le immagini pronte, le aggiungiamo alle pagine corrispondenti (Home, Chi siamo, Prodotti, Ricette).

## Form di contatto
Il form usa Formspree. Prima di andare online, sostituisci `TU_ID_FORMSPREE` nei file:
- `src/pages/contacto.astro`
- `src/pages/it/contatti.astro`
- `src/pages/en/contact.astro`
- `src/pages/ca/contacte.astro`

con l'ID del tuo account Formspree gratuito (formspree.io).

## Dominio personalizzato
Il file `public/CNAME` contiene già `makkeroni.com`. Una volta che il sito è online su GitHub Pages, va aggiornato il DNS del dominio (presso il tuo registrar) puntando ai server di GitHub Pages — istruzioni esatte quando siamo a quel punto.
