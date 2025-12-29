# ⚽ Football Shotmaps

Application de visualisation et d'analyse des zones de tir pour les principales compétitions de football européennes.

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![Streamlit](https://img.shields.io/badge/streamlit-1.28+-red.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 🌟 Fonctionnalités

### 📊 Visualisation
- **Shotmaps détaillées** avec hexbins de densité
- **Photos des joueurs** intégrées automatiquement
- **Logos des équipes** en temps réel
- **Statistiques complètes** : tirs, buts, xG, précision, distance médiane
- **Filtres avancés** : par équipe, type d'analyse, nombre de joueurs
- **Modes d'affichage** : large, compact ou grille

### 🔄 Collecte de données
- **Scraping automatisé** depuis FotMob
- **7 compétitions** : Ligue 1, Premier League, La Liga, Bundesliga, Serie A, Champions League, Europa League
- **Historique** : données disponibles depuis 2020/2021
- **Exclusion automatique** des penalties

### 🎨 Design
- **Interface ultra-moderne** avec thèmes par ligue
- **Animations fluides** et transitions élégantes
- **Responsive** : adapté à tous les écrans
- **Police personnalisée** : Montserrat & Inter

## 📸 Aperçu

L'application propose des shotmaps avec :
- Hexbins de densité colorés selon le thème de la ligue
- Demi-cercle de distance médiane de tir
- Statistiques détaillées (tirs, buts, xG, xG/tir)
- Distance médiane et précision
- Photos et logos en haute résolution

## 🚀 Installation

### Prérequis
- Python 3.8 ou supérieur
- pip

### Installation des dépendances

```bash
# Cloner le repository
git clone https://github.com/votre-username/football-shotmaps.git
cd football-shotmaps

# Installer les packages
pip install -r requirements.txt
```

## 💻 Utilisation

### Lancer l'application

```bash
streamlit run app.py
```

L'application s'ouvrira automatiquement dans votre navigateur à l'adresse `http://localhost:8501`

### Mode Visualisation

1. Sélectionnez une **compétition**
2. Choisissez une **saison**
3. Filtrez par **équipe** (optionnel)
4. Sélectionnez le **type d'analyse** :
   - Top Tireurs
   - Meilleurs Buteurs
   - Meilleur xG
5. Ajustez le **nombre de joueurs** et la **taille d'affichage**

### Mode Collecte

1. Sélectionnez une **compétition**
2. Choisissez une **saison**
3. Cliquez sur **🚀 Lancer la collecte**
4. Attendez la fin du scraping (barre de progression)
5. Les données sont sauvegardées automatiquement en CSV

## 📁 Structure du projet

```
football-shotmaps/
│
├── app.py                      # Application principale
├── requirements.txt            # Dépendances Python
├── README.md                   # Documentation
├── LICENSE                     # Licence MIT
├── .gitignore                 # Fichiers à ignorer
│
├── data/                       # Données collectées (CSV)
│   └── .gitkeep
│
└── assets/                     # Assets (si nécessaire)
    └── .gitkeep
```

## 🏆 Compétitions supportées

| Compétition | ID | Saisons disponibles |
|------------|----|--------------------|
| Ligue 1 | 53 | 2020/21 - 2025/26 |
| Premier League | 47 | 2020/21 - 2025/26 |
| La Liga | 87 | 2020/21 - 2025/26 |
| Bundesliga | 54 | 2020/21 - 2025/26 |
| Serie A | 55 | 2020/21 - 2025/26 |
| Champions League | 42 | 2020/21 - 2025/26 |
| Europa League | 73 | 2020/21 - 2025/26 |

## 🔧 Technologies utilisées

- **Streamlit** : Framework d'application web
- **Pandas** : Manipulation de données
- **Matplotlib** : Visualisation
- **mplsoccer** : Terrains de football
- **Requests** : Requêtes HTTP
- **Pillow** : Traitement d'images
- **NumPy** : Calculs numériques

## 📊 Format des données

Les données sont sauvegardées en CSV avec les colonnes suivantes :

- `match_id` : Identifiant du match
- `ligue` : Nom de la compétition
- `saison` : Saison (format YYYY/YYYY)
- `date` : Date du match (UTC)
- `type_evenement` : Type de tir (Goal, SavedShot, etc.)
- `equipe_id` : ID de l'équipe
- `joueur` : Nom du joueur
- `equipe_joueur` : Nom de l'équipe
- `joueur_id` : ID du joueur
- `minute` : Minute du tir
- `xg` : Expected Goals
- `situation` : Contexte du tir
- `position_x` : Coordonnée X
- `position_y` : Coordonnée Y

## ⚠️ Notes importantes

- Les **penalties sont exclus** de toutes les analyses
- Le scraping respecte un délai de **0.3s** entre chaque requête
- Les headers HTTP sont nécessaires pour accéder à l'API FotMob
- Les images sont téléchargées en temps réel depuis FotMob



## 📝 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.
