# Détection de Comptes Automatisés (Bots) sur VK

## Contexte
VK (VKontakte) est un réseau social majeur en Russie.  
Comme toute plateforme sociale, il est affecté par des **comptes automatisés (bots)** utilisés pour le spam,
la manipulation d’opinion ou la collecte de données.

## Objectif
Détecter automatiquement les **comptes bots vs humains** à partir de métadonnées utilisateurs
en utilisant des techniques de **Data Mining et Machine Learning interprétables**.

## Dataset
- **Source** : Kaggle – Users vs Bots Classification
- **Lien** : https://www.kaggle.com/datasets/akshatsharma24/users-vs-bots-classification
- **Observations** : comptes VK
- **Cible** :
  - `0` → Bot
  - `1` → Humain

> Le dataset n’est pas inclus dans ce dépôt pour des raisons de taille.

## Méthodologie
1. Analyse exploratoire (EDA)
2. Nettoyage & prétraitement (variables quantitatives & qualitatives)
3. Feature engineering (engagement, activité, richesse du contenu)
4. Équilibrage des classes (SMOTE)
5. Modélisation & comparaison de modèles
6. Interprétabilité des résultats (SHAP, LIME)

## Modèles utilisés
- Logistic Regression (avec sélection de variables)
- Decision Tree (RFE)
- Random Forest (Grid Search)
- Bagging & AdaBoost
- SVM

## Évaluation
- ROC-AUC
- Confusion Matrix
- Precision / Recall / F1-score
- Validation croisée (StratifiedKFold)

## Interprétabilité
- **SHAP** : importance globale des variables
- **LIME** : explication locale des prédictions individuelles

## Résultats clés
- Très forte capacité de discrimination bots / humains (ROC-AUC élevé)
- Variables les plus importantes :
  - `engagement_score`
  - `posts_per_day`
  - `reposts_ratio`
- Modèles interprétables avec règles claires (Decision Tree)

## Technologies
Python, Pandas, NumPy, Scikit-learn, Imbalanced-learn, SHAP, LIME, Matplotlib, Seaborn

## Exécution
```bash
1. Télécharger le dataset depuis Kaggle
2. Lancer `VK_Bots_Detection.ipynb`

## Auteur
Chaima Khemiri
