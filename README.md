# DataTouch AI

> Dashboard de données 3D interactif, piloté par reconnaissance de gestes de la main, avec insights générés par intelligence artificielle en temps réel.

![status](https://img.shields.io/badge/status-en%20d%C3%A9veloppement-yellow)
![license](https://img.shields.io/badge/license-MIT-blue)

---

## Le concept

DataTouch AI transforme l'exploration de données en expérience physique. Plutôt que de cliquer sur des graphiques avec une souris, l'utilisateur **interagit avec ses mains** face à sa webcam : il attrape, fait pivoter et zoome sur des visualisations 3D flottantes. Quand un élément est sélectionné, une IA génère instantanément une explication contextuelle de la donnée affichée.

Ce projet combine trois domaines : la visualisation de données, l'interaction homme-machine par computer vision, et l'IA générative.

## Démo

<!-- Ajouter ici un GIF ou lien vers la vidéo de démo -->
`[GIF de démonstration à venir]`

## Fonctionnalités

- Visualisation de données sous forme d'objets 3D interactifs
- Détection de gestes (pincer pour sélectionner, écarter pour zoomer, déplacer pour tourner) via la webcam
- Génération d'insights en langage naturel via l'API Claude à chaque sélection
- Interface immersive sans clic ni clavier

## Stack technique

| Domaine | Technologie |
|---|---|
| Rendu 3D | [Three.js](https://threejs.org) |
| Suivi des mains | [MediaPipe Hands](https://developers.google.com/mediapipe) |
| Intelligence artificielle | [Anthropic Claude API](https://www.anthropic.com) |
| Traitement des données | PapaParse (CSV) |
| Build tool | Vite |
| Déploiement | Vercel |

## Installation

```bash
# Cloner le dépôt
git clone https://github.com/fatimazahraBe/datatouch-ai.git
cd datatouch-ai

# Installer les dépendances
npm install

# Configurer les variables d'environnement
cp .env.example .env
# Ajouter ta clé API Anthropic dans .env

# Lancer en local
npm run dev
```

L'application s'ouvre sur `http://localhost:5173`. Autorise l'accès à ta webcam pour activer le hand tracking.

## Structure du projet

```
datatouch-ai/
├── src/
│   ├── main.js              # Point d'entrée, boucle de rendu
│   ├── scenes/               # Construction de la scène 3D
│   ├── data/                 # Chargement et transformation des données
│   ├── ai/                   # Intégration de l'API Claude
│   └── utils/                # Détection des gestes
├── public/data/               # Datasets utilisés
└── index.html
```

## Données utilisées

Ce projet utilise un jeu de données de ventes (Superstore Dataset) à des fins de démonstration. Voir `src/data/` pour la logique de transformation.

## Roadmap

- [x] Setup Three.js + rendu de base
- [x] Intégration du hand tracking
- [x] Génération des visualisations depuis les données
- [x] Interaction gestuelle (sélection, zoom, rotation)
- [x] Intégration de l'IA pour les insights
- [ ] Support de datasets personnalisés (upload CSV)
- [ ] Mode multi-utilisateurs

## Auteure

**Fatimazahra Bellala** — Data Analyst
- GitHub : [@fatimazahraBe](https://github.com/fatimazahraBe)
- LinkedIn : [fatimazahra-bellala](https://linkedin.com/in/fatimazahra-bellala)

## 📄 Licence

Ce projet est sous licence MIT — voir le fichier [LICENSE](LICENSE) pour plus de détails.
