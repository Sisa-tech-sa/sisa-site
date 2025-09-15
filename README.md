# SISA — Staging Workbench

Prévisualisation des pages HTML avant migration vers Cloudflare Pages.  
Date: 2025-09-15

## Structure
- `index.html` — lanceur vers toutes les pages
- `SISA_hebergement.html` — page offre hébergement
- `SISA_Liste_Achats.html` — checklist interactive
- `SISA_PACK_Intranet.html` — pack v1
- `SISA_PACK_Intranet_v2.html` — pack v2 (fournisseurs + coûts)
- `SISA_PACK_Intranet_v3_WIFI.html` — pack v3 (Wi-Fi)
- `SISA_Meme_5G.html` — éditeur de mème
- `assets/` — images, etc.

## Déploiement GitHub Pages (branche `main`)
1. Créez un dépôt vide sur GitHub (ex. `sisa-staging`).
2. Téléversez tous les fichiers de ce dossier à la racine.
3. Dans **Settings → Pages**, choisissez *Deploy from a branch* → `main` (`/`).

## Migration “propre” vers Cloudflare Pages
1. Sur Cloudflare Pages: **Create project** → **Connect to Git** → choisissez le même repo.
2. Framework: **None** (site statique), Build command: *(vide)*, Output folder: `/`.
3. Une fois en ligne: attachez votre domaine (Records DNS gérés par Cloudflare).

> Astuce: ajoutez un fichier `.nojekyll` à la racine pour éviter tout traitement Jekyll côté GitHub Pages.
