# 📊 Carte de Risque IA
### Projet Data Science 2 – Santé financière & Profilage d’entreprises

## 🎯 Objectif
Classification des entreprises selon leur santé financière via le Scoring Métier et Scoring ML.

## 🧩 Problématique
> Peut-on classifier les entreprises selon leur niveau de risque afin de détecter des profils homogènes et orienter des actions de pilotage ?

## 📂 Dataset
- Fichier : `Data_09092025.xlsx`
- 4 254 lignes — 885 entreprises — 6 secteurs — 5 années  
- Variables : ratios financiers, marges, délais, rentabilité, structure du bilan, etc.
  #### 🔗 Données brutes du projet

Les données brutes utilisées dans ce projet sont disponibles ici :  
👉 [Lien vers les données brutes](https://urlz.fr/uYLr)

## 🔍 Étapes réalisées dans la mission
## Etape1 Préparation des données
- Inspection des dimensions et types
- Traitement des valeurs manquantes et valeurs aberrantes
- Détection et suppression des doublons
- Statistiques descriptives par variable
- Visualisations : histogrammes, boxplots, heatmaps
- Création d'un Feature Store (DataFrame enrichi) avec :
- Ratios standardisés (z-score/quantiles).
- Nouveaux indicateurs : DSO–DPO (BFR), Croissance CA, Volatilité marge.

## Etape 2 Scoring avancé:
- Scoring métier pondéré :
- Liquidité (25 %), Rentabilité (25 %), BFR (20 %), Fiscalité (15 %), Structure
(15 %).
- Machine Learning supervisé (labels disponibles) :
-Entrainement du Modèle par Random Forest pour prédire "Risque Haut vs Bas".
 Combinaison Score métier + Score ML pour un score final hybride.

## Etape 3. Détection d’anomalies par secteur d'entreprises
 Implémentation de  3 méthodes :
o Isolation Forest,
o Local Outlier Factor (LOF),
o DBSCAN (clustering).
 Comparaison des résultats de 3 méthodes avec un indice d’anomalie consolidé.

## Evaluation du Modèle ML par les métriques
MÉTRIQUES DE QUALITÉ:
   • Model ML Accuracy: 0.952
   • Model ML AUC-ROC: 0.991
   • Cohérence anomalies (3 méthodes): 125 entreprises
   • Couverture complète: 100% des données
   
## 🧠 Méthodologie — Clustering
**Préparation**
- Sélection et normalisation des variables
- Imputation des valeurs manquantes par normalisation par secteur/année Imputation par la médiane par secteu/année
- Réduction dimensionnelle (PCA)

**Algorithmes testés**
- DBSCAN, Agglomerative Clustering en comparaison
- Local Outlier Factor (LOF)
- IsolationForest(détection des valeurs aberrantes)
- IQR(détection des valeurs manquantes)


## ▶️ Exécution
```bash
pip install -r requirements.txt
jupyter notebook notebooksPeut-on classer les entreprises selon leur santé financière via le Scoring Métier et le Scoring ML afin orienter des actions de pilotage ?.ipynb
```

## 📁 Structure du repo
```
├── data/                     
├── notebooks/
│   └── Mission 2_Carte de Risque IA_Niveau Avancé_Mohamadou_Hayatou.ipynb
├── src/
│   ├── preprocessing.py
│   ├── clustering.py
│   ├── feature engineering and ML.py
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
