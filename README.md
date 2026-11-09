# Boîte à outils

Des outils prêts à servir pour tous vos projets : vidéo, IA, documents, gestion.
Site statique : tout fonctionne dans le navigateur, sans serveur, et les fichiers de l'utilisateur restent sur son appareil.

| Outil | Page | Ce qu'il fait |
|---|---|---|
| Studio vidéo IA | `studio.html` | Fond, personnage animé, voix IA et sous-titres réunis dans une vidéo (WebM ou MP4) |
| Voix IA | `voix.html` | Texte → voix française (WAV) |
| Sous-titres IA | `sous-titres.html` | Transcription automatique (SRT, VTT) et incrustation dans la vidéo |
| Détourage IA | `detourage.html` | Retirer le fond d'une photo (personnes, objets, produits, véhicules) |
| Atelier vidéo | `video.html` | Couper, compresser, convertir en GIF, extraire le son |
| Documents PDF | `documents.html` | Devis en PDF, fusion de PDF, lecture de PDF |
| Tableur | `tableur.html` | Ouvrir, modifier et enregistrer des fichiers Excel ou CSV ; modèle de suivi des dossiers |

## Modèles d'IA

Les moteurs d'IA tournent dans le navigateur. Les modèles sont téléchargés depuis huggingface.co au premier usage, puis gardés en cache par le navigateur :

| Usage | Modèle | Taille | Licence |
|---|---|---|---|
| Voix « Siwis » (femme) | Piper fr_FR-siwis-medium | ≈ 60 Mo | CC-BY 4.0 : citer « voix SIWIS » |
| Voix « Gilles » (homme) | Piper fr_FR-gilles-low | ≈ 60 Mo | CC0 |
| Voix « UPMC » (femme) | Piper fr_FR-upmc-medium | ≈ 75 Mo | CC-BY-SA 4.0 |
| Sous-titres rapides | Whisper base | ≈ 80 Mo | MIT |
| Sous-titres précis | Whisper small | ≈ 250 Mo | MIT |
| Détourage de personnes | MODNet | ≈ 7 Mo | Apache 2.0 |
| Détourage d'objets | ORMBG | ≈ 45 Mo | Apache 2.0 |

Ce qui n'est pas possible dans un navigateur : générer des images ou des vidéos entières par IA (décors, personnages réalistes, avatars qui parlent à partir d'une photo). Ces modèles demandent une carte graphique puissante sur un serveur.

## Vidéos d'annonce en série (Remotion)

Le dossier `video/` crée une vidéo verticale (TikTok, Reels, statut WhatsApp) : étiquette, titre, détails, prix et une dernière ligne.

- **Depuis GitHub, sans rien installer** : onglet **Actions → Créer une vidéo d'annonce → Run workflow**, puis téléchargez la vidéo dans **Artifacts**.
- **Sur un ordinateur** : `cd video && npm install && npm run studio` pour modifier le modèle en direct.

Remotion est gratuit pour les particuliers et les petites entreprises ; une entreprise plus grande a besoin d'une licence payante (voir remotion.dev/license).

## Vérification automatique

À chaque envoi sur GitHub, l'action **Vérification du site** contrôle que tous les liens, images et scripts des pages existent (`scripts/verifier-liens.mjs`).

## Logiciels libres inclus

| Outil | Version | Licence | Emplacement |
|---|---|---|---|
| jsPDF | 4.2.1 | MIT | `lib/jspdf/` |
| pdf-lib | 1.17.1 | MIT | `lib/pdf-lib/` |
| PDF.js | 6.4.299 | Apache 2.0 | `lib/pdfjs/` |
| SheetJS (édition communautaire) | 0.20.3 | Apache 2.0 | `lib/sheetjs/` |
| ffmpeg.wasm | 0.12.15 | MIT | `lib/ffmpeg/` (le moteur FFmpeg, GPL, est chargé depuis cdn.jsdelivr.net) |
| transformers.js | 4.3.1 | Apache 2.0 | chargé depuis cdn.jsdelivr.net par `ia.js` ; ses fichiers ONNX Runtime sont dans `lib/transformers/` |
| ONNX Runtime Web | 1.30.0 et 1.31.0-dev | MIT | `lib/onnxruntime/`, `lib/transformers/` |
| piper-tts-web, piper-wasm | 1.0.5, 1.0.0 | MIT (données eSpeak NG : GPL-3.0) | `lib/piper/` |
| Police DejaVu Sans | – | licence libre DejaVu | `lib/polices/` |
| Remotion | 4.0.537 | Licence Remotion | `video/` (installé par npm) |

Le fichier de licence de chaque outil se trouve dans son dossier.
