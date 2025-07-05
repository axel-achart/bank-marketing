# 🏦 Projet : Prédiction de souscription à une offre bancaire

## 🎯 Objectif

L'objectif de ce projet est de construire un modèle de classification supervisée capable de prédire si un client souscrira à une offre de **dépôt à terme** suite à une campagne de marketing téléphonique.

Nous utilisons pour cela le jeu de données **Bank Marketing UCI**, ainsi que la librairie **PyCaret** qui permet une modélisation rapide grâce à l’AutoML.

---

## 📂 Contenu du projet

Le repository contient :
- `exploration.ipynb` : analyse exploratoire des données
- `modelisation.ipynb` : entraînement et évaluation de modèles avec PyCaret
- `README.md` : ce fichier

---

## 🧠 Partie 1 – Veille théorique

### 🔍 Notions clés de l'apprentissage automatique supervisé

- **Apprentissage supervisé** : Apprentissage à partir de données étiquetées pour prédire une cible.
- **Données labellisées** : Données avec une réponse connue (ex. : "yes" ou "no").
- **Classification supervisée** : Prédiction d’une catégorie (ex. : dépôt souscrit ou non).
- **Modèle d’apprentissage automatique** : Programme qui apprend à partir de données pour faire des prédictions.
- **Données d’entraînement** : Données utilisées pour entraîner le modèle.
- **Target** : Variable cible à prédire (`y` dans ce projet).
- **Phase d’entraînement** : Le modèle apprend à reconnaître les patterns dans les données.
- **Phase de prédiction** : Le modèle applique ce qu’il a appris à de nouvelles données.
- **Prétraitement** : Nettoyage et préparation des données avant modélisation (suppression des valeurs manquantes, encodage, etc.).
- **Accuracy** : Pourcentage de bonnes prédictions. Exemple : 85% de précision = 85 prédictions correctes sur 100.
- **AutoML** : Automatisation du machine learning (test automatique de plusieurs modèles).
- **Arbre de décision** : Modèle qui prend des décisions via des règles ("si... alors...").

---

## 📊 Partie 2 – Analyse des données

### 📁 Dataset

Le jeu de données contient des informations sur des clients contactés dans le cadre de campagnes marketing d'une banque portugaise.

Chaque ligne représente un client, avec les colonnes suivantes (extrait) :
- `age` : âge du client
- `job` : type d’emploi
- `marital` : état civil
- `education` : niveau d’étude
- `balance` : solde du compte
- `contact`, `month`, `duration`... : infos sur la campagne
- `poutcome` : résultat d’une campagne précédente
- **`y`** : **variable cible** indiquant si le client a souscrit à l’offre

### 🧹 Prétraitement effectué

- Suppression des valeurs `unknown` remplacées par `NaN`
- Suppression des lignes incomplètes (`dropna`)
- Transformation automatique des variables catégorielles via PyCaret

### 📈 Analyse exploratoire (voir `exploration.ipynb`)

- Répartition de la variable cible : déséquilibrée (`no` majoritaire)
- Profils d’âge des clients : 30–60 ans
- Taux de souscription plus élevé chez les étudiants, retraités, cadres

---

## 🤖 Partie 3 – Modélisation avec PyCaret

### ⚙️ Outil utilisé

[PyCaret](https://pycaret.gitbook.io/docs/) est une librairie Python AutoML low-code permettant de tester rapidement plusieurs modèles de machine learning.

### 🔁 Étapes suivies

1. Initialisation de PyCaret avec `setup()`
2. Comparaison automatique des modèles avec `compare_models()`
3. Sélection du meilleur modèle selon la **métrique d’accuracy**
4. Finalisation et test du modèle

### 📊 Résultats

Le meilleur modèle sélectionné par PyCaret (ex. : `RandomForestClassifier`, `GradientBoostingClassifier`, ou autre selon l'exécution) a permis d’atteindre une **accuracy supérieure à 85 %**.

Ce modèle est capable de prédire correctement dans la majorité des cas si un client est susceptible de souscrire.

---

## ✅ Conclusion

Ce projet a permis de :
- Comprendre les étapes clés de l’apprentissage automatique supervisé
- Nettoyer et analyser un jeu de données réel
- Utiliser PyCaret pour entraîner et comparer des modèles rapidement
- Construire un outil de prédiction basé sur des données client

Grâce à cette approche, la banque pourrait **mieux cibler ses campagnes** marketing et augmenter son taux de conversion client.

---

## 🔗 Ressources utilisées

- 📘 PyCaret Docs : [https://pycaret.gitbook.io/docs](https://pycaret.gitbook.io/docs)
- 📹 StatQuest YouTube : [A Gentle Introduction to ML](https://www.youtube.com/watch?v=Gv9_4yMHFhI)
- 📝 Classification Blog – DataCamp : [Introduction à la classification](https://www.datacamp.com/blog/classification-machine-learning)

