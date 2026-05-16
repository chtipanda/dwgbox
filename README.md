# 🪵 DwgBox — Générateur Boîte CNC

Générateur paramétrique de boîtes en bois pour CNC 3 axes.  
Export DXF compatible **Aspire (Vectric)**, **CamBam**, **Krabscam**.

**→ [Ouvrir l'application](https://chtipanda.github.io/dwgbox/)**  
**→ [Lire l'article de présentation](https://chtipanda.github.io/dwgbox/article.html)**

---

## Fonctionnalités

- **3 formes** : rectangulaire, ronde, hexagonale
- **2 types d'emboîtement** : recouvrement ou intérieur
- Calcul automatique du **déport ball-nose** (fond de boîte)
- **Jeu fonctionnel** paramétrable, appliqué sur le tenon
- Détection d'erreurs en temps réel (tenon trop mince, fraise trop grande…)
- Export **DXF AC1009** (R12) multi-couches, sans polylignes ni splines
- **PWA** — fonctionne hors ligne après premier chargement

## Structure DXF

| Couche | Contenu |
|--------|---------|
| `CONTOUR_EXT` | Contour extérieur — découpe |
| `CAVITE_INT` | Cavité intérieure — poche |
| `FOND_BALLNOSE` | Chemin fond déporté Ø/2 — ball-nose |
| `RAINURE_EXT` | Bord extérieur de la rainure |
| `RAINURE_INT` | Bord intérieur de la rainure |

## Déploiement local

Aucune dépendance. Ouvrir `index.html` dans un navigateur.  
Pour le Service Worker (PWA), servir via HTTPS ou `localhost`.

```bash
# Serveur local rapide
python3 -m http.server 8080
# puis ouvrir http://localhost:8080
```

## Structure du dépôt

```
dwgbox/
├── index.html      Application principale
├── article.html    Article de présentation
├── sw.js           Service Worker (cache offline)
├── manifest.json   Manifest PWA
├── icon-192.svg    Icône 192×192
├── icon-512.svg    Icône 512×512
└── README.md       Ce fichier
```

## Licence

MIT — libre d'utilisation, de modification et de redistribution.

---
*Par [chtipanda](https://github.com/chtipanda)*
