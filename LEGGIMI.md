# Ordini online Mr Wu (Geri)

Sito statico: nessun build. Supabase: https://tsgxnsvwglhebgelwaxn.supabase.co

| Pagina | Indirizzo | A cosa serve |
|---|---|---|
| Pannello admin | `/` (index.html) | menu, prodotti, ordini, **Tavoli** (AYCE, QR) |
| Ordini asporto | `/ordina/` | apre ordina.html del locale Mr Wu |
| Ordine al tavolo | `/tavolo.html?tenant=...&tavolo=N` | si apre dai QR (stampali da admin → Tavoli) |

## Pubblicazione
1. GitHub → New repository (es. `OrdiniGeri`, anche privato) → "uploading an existing file"
   → trascina **il contenuto** di questa cartella (non la cartella stessa) → Commit.
2. Cloudflare → Workers & Pages → Create → Pages → Connect to Git → scegli il repo.
   Framework preset: **None**, Build command: **vuoto**, Build output directory: **/**  → Save and Deploy.
3. Supabase → Authentication → URL Configuration → Site URL = l'indirizzo `*.pages.dev`
   (serve per i link delle email di conferma/recupero password).
4. Apri l'indirizzo, entra con l'admin, poi dallo spooler "Importa catalogo sul sito".

Ogni modifica caricata su GitHub viene pubblicata da Cloudflare in automatico in 1-2 minuti.
