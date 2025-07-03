# Fiche Readme

## Contexte du projet
Ce projet de data science s'appuie sur le dataset **Bank Marketing UCI**, issu d'une banque portugaise, qui contient des données collectées lors de **campagnes de marketing téléphonique** visant à inciter les clients à souscrire à un **dépôt à terme**.

Chaque enregistrement représente une interaction client avec des informations telles que :
- Des **données démographiques** (âge, emploi, niveau d'études, état civil, etc.),
- Des **informations comportementales** (nombre de contacts, durée des appels, résultats de campagnes précédentes...),
- Et une **variable cible** indiquant si le client a souscrit ou non au dépôt proposé.

Ce projet vise à :
- **Analyser** les données pour mieux comprendre les caractéristiques influençant la souscription,
- **Prétraiter** les données pour les rendre exploitables,
- **Développer un modèle de classification supervisée** capable de prédire l’issue d’une campagne auprès d’un client,
- **Automatiser** ce processus via **PyCaret**, une librairie AutoML open-source qui permet d'entraîner, comparer et sélectionner des modèles de machine learning de manière rapide et efficace.

L'approche pédagogique comprend :
- Une **veille préalable** sur les concepts de machine learning supervisé (classification, arbre de décision, target, accuracy...),
- Un **nettoyage et une exploration des données** via Pandas,
- L'utilisation de **PyCaret** pour configurer, entraîner et évaluer automatiquement plusieurs modèles de classification,
- L'interprétation des résultats pour choisir le meilleur modèle selon la **métrique d’accuracy**.

Ce projet permet de se familiariser avec l’ensemble du pipeline de machine learning, depuis la compréhension métier jusqu’à la modélisation automatisée, tout en développant des compétences concrètes en **data science**, **analyse exploratoire**, **apprentissage automatique** et **AutoML**.

---

## Les données et leur analyse

---

## Les algorithmes utilisés

---

## Conclusion du travail

---

## Veille réalisée
1) Qu’est-ce que l’apprentissage automatique supervisé ?
C’est quand un ordinateur apprend à partir d’exemples déjà résolus (appelés données étiquetées) pour faire des prédictions sur de nouvelles données. On lui montre quoi faire, et il apprend à imiter.

2) Qu’est-ce que les données étiquetées (ou labellisées) ?
Ce sont des données avec une réponse connue. Par exemple, une image de chat avec l’étiquette "chat", ou un e-mail avec l’étiquette "spam".

3) En particulier, qu’est-ce que la classification supervisée (ou méthode de classement) ?
C’est un type d’apprentissage supervisé où le modèle apprend à classer les données dans des catégories (ex : "chat" ou "chien").

4) Qu’est-ce qu’un modèle d’apprentissage automatique ?
C’est un programme informatique qui apprend à partir des données pour ensuite faire des prédictions.

5) Qu’est-ce que les données d’entraînement ? Qu’est-ce que l’entraînement d’un modèle de classification supervisée ?
Les données d’entraînement sont celles qu’on utilise pour apprendre au modèle. L’entraînement, c’est le processus où le modèle apprend les règles pour classer les données correctement.

6) Qu’est-ce que la donnée cible (ou le target) ?
C’est la réponse qu’on veut prédire. Exemple : pour un mail, le target peut être "spam" ou "non spam".

7) À quoi sert la phase d’entraînement d’un modèle d’apprentissage automatique ?
Elle sert à apprendre à partir des données connues. C’est à ce moment que le modèle découvre comment résoudre le problème.

8) À quoi sert la phase de prédiction d’un modèle d’apprentissage automatique ?
Une fois entraîné, le modèle peut être utilisé pour faire des prédictions sur de nouvelles données inconnues.

9) Qu’est-ce que le prétraitement des données et pourquoi est-il important à réaliser avant l'entraînement d'un modèle d'apprentissage automatique ?
C’est la phase où on nettoie et prépare les données (ex : enlever les valeurs manquantes, normaliser...). C’est essentiel car des données mal préparées donnent un mauvais modèle.

10) Comment l’évaluation d’un modèle d’apprentissage automatique pour une tâche de classification peut-elle se faire ? 
Etudiez en particulier et seulement, la métrique d’accuracy. En quoi est-elle un indicateur de performance d’un modèle ?
L’accuracy mesure le pourcentage de bonnes prédictions faites par le modèle.
Par exemple : 90 bonnes réponses sur 100 → accuracy = 90%.
C’est un indicateur simple de performance.

11) Qu’est ce que l’AutoML et pourquoi est-il pertinent pour vous en tant que débutant dans le domaine de l’intelligence artificielle ?
L’AutoML automatise la création de modèles d’IA (choix du modèle, réglages, etc.).
C’est utile pour les débutants car ça simplifie le processus sans avoir besoin de tout maîtriser. Et puis ça empêche la démotivation aux gens moins persévérant.

12) Qu’est ce qu’un arbre de décision pour la classification supervisée ? Comment fonctionne–t-il ?
C’est un modèle qui prend des décisions en suivant un chemin de questions.
Exemple :
Animal a-t-il 4 pattes ? → Oui
Est-ce qu’il miaule ? → Oui → Chat
Il apprend ces questions à partir des données. Très visuel et facile à comprendre !