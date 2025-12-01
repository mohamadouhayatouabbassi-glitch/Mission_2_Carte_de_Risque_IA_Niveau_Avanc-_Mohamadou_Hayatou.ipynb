# 📊 Analyse et Clustering de Données Financières d’Entreprises
### Projet Data Science – Santé financière & Profilage d’entreprises

## 🎯 Objectif
Segmenter les entreprises selon leur santé financière pour détecter des profils homogènes et orienter des actions de pilotage.

## 🧩 Problématique
> Peut-on regrouper les entreprises selon leur santé financière afin de détecter des profils homogènes et orienter des actions de pilotage ?

## 📂 Dataset
- Fichier : `Data_09092025.xlsx`
- 4 254 lignes — 885 entreprises — 6 secteurs — 5 années  
- Variables : ratios financiers, marges, délais, rentabilité, structure du bilan, etc.
  #### 🔗 Données brutes du projet

Les données brutes utilisées dans ce projet sont disponibles ici :  
👉 [Lien vers les données brutes](https://urlz.fr/uYLr)

## 🔍 Étapes réalisées (EDA)
- Inspection des dimensions et types
- Traitement des valeurs manquantes et valeurs aberrantes
- Détection et suppression des doublons
- Statistiques descriptives par variable
- Visualisations : histogrammes, boxplots, heatmaps

## 📈 Visualisations avancées
- Heatmap de corrélation
- Boxplots par secteur
- PCA pour réduction de dimension
- Projection 2D des clusters (PCA / t-SNE)

## 🧠 Méthodologie — Clustering
**Préparation**
- Sélection et normalisation des variables
- Imputation des valeurs manquantes si nécessaire
- Réduction dimensionnelle (PCA)

**Algorithmes testés**
- KMeans (principal)
- DBSCAN, Agglomerative Clustering en comparaison
- IsolationForest(détection des valeurs aberrantes)
- IQR(détection des valeurs manquantes)


## ▶️ Exécution
```bash
pip install -r requirements.txt
jupyter notebook notebooksPeut-on regrouper les entreprises selon leur santé financière afin de détecter des profils homogènes et orienter des actions de pilotage ?.ipynb
```

## 📁 Structure du repo
```
├── data/                     
├── notebooks/
│   └── Mission 1_Exploration et Valorisation des données financières _Mohamadou Hayatou Abbassi.ipynb
├── src/
│   ├── preprocessing.py
│   ├── clustering.py
│   ├── visualization.py
├── reports/
│   ├── rapport.pdf
│   └── presentation.pdf
├── README.md
├── requirements.txt
└── .gitignore
```

## 🧰 Librairies principales
pandas, numpy, scikit-learn, matplotlib, seaborn, plotly,

## 📄 Livrables
- Notebook Jupyter commenté
- Rapport / Présentation (PDF)
- Scripts modulaires dans `src/`

## 👤 Auteur
**Mohamadou Hayatou Abbassi**
