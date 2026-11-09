# Boîte à outils

Des outils prêts à servir pour tous vos projets : devis, PDF, tableaux et suivi des dossiers.
Site statique : tout fonctionne dans le navigateur, sans serveur, et les fichiers de l'utilisateur restent sur son appareil.

| Outil | Page | Ce qu'il fait |
|---|---|---|
| Documents PDF | `documents.html` | Devis en PDF, fusion de PDF, lecture de PDF |
| Tableur | `tableur.html` | Ouvrir, modifier et enregistrer des fichiers Excel ou CSV ; modèle de suivi des dossiers |

Les outils vidéo et IA (studio vidéo IA, voix, sous-titres, détourage, motion design) sont dans le dépôt séparé `cr-ateur-vid-o-ia-` (Créateur vidéo IA).

## Vérification automatique

À chaque envoi sur GitHub, l'action **Vérification du site** contrôle que tous les liens, images et scripts des pages existent (`scripts/verifier-liens.mjs`).

## Logiciels libres inclus

| Outil | Version | Licence | Emplacement |
|---|---|---|---|
| jsPDF | 4.2.1 | MIT | `lib/jspdf/` |
| pdf-lib | 1.17.1 | MIT | `lib/pdf-lib/` |
| PDF.js | 6.4.299 | Apache 2.0 | `lib/pdfjs/` |
| SheetJS (édition communautaire) | 0.20.3 | Apache 2.0 | `lib/sheetjs/` |

Le fichier de licence de chaque outil se trouve dans son dossier.

