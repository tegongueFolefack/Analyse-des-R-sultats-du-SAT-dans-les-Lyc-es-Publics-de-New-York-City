# 🏫 Analyse des Performances SAT des Écoles Publiques de New York City

![New York City schoolbus](schoolbus.jpg)  
📷 *Photo by [Jannis Lucas](https://unsplash.com/@jannis_lucas) on [Unsplash](https://unsplash.com)*

---

## 📘 Contexte

Les **SATs** (Scholastic Assessment Tests) sont des examens standardisés utilisés aux États-Unis pour mesurer les compétences des élèves en **mathématiques**, **lecture** et **écriture**.  
Chaque section est notée sur **800 points**, pour un score total maximal de **2400**.

Ces résultats jouent un rôle central dans les processus d’admission à l’université, mais servent également de référence pour évaluer la performance académique des établissements.

---

## 🎯 Objectifs du Projet

Ce projet a pour but d'explorer les scores SAT des lycées publics de **New York City (NYC)** à partir du fichier `schools.csv`, à travers les objectifs suivants :

1. 🧮 Identifier les écoles ayant les **meilleurs résultats en mathématiques**
2. 🏆 Trouver les **10 meilleures écoles** selon le **score SAT total**
3. 📊 Déterminer **l’arrondissement** avec la **plus grande variabilité des scores SAT combinés**

---

## 🧾 Structure des Données

Les données proviennent du fichier `schools.csv`, contenant les colonnes suivantes :

| Colonne            | Description                                      |
|--------------------|--------------------------------------------------|
| `school_name`      | Nom de l'établissement scolaire                  |
| `borough`          | Arrondissement de New York (e.g., Manhattan)     |
| `average_math`     | Score moyen en mathématiques                     |
| `average_reading`  | Score moyen en lecture                           |
| `average_writing`  | Score moyen en écriture                          |

> 🔎 Chaque section SAT est notée sur **800 points**, soit un total possible de **2400 points**.

---

## 🧪 Méthodologie & Résultats

### 1. 🧮 Meilleures Écoles en Mathématiques

- **Critère de sélection :** `average_math >= 640` (équivaut à 80 % de 800)
- **Résultat stocké dans :** `best_math_schools`
- **Colonnes retournées :** `school_name`, `average_math`
- **Ordre de tri :** décroissant selon `average_math`

📈 _Visualisation :_ Histogramme des scores en mathématiques

---

### 2. 🏆 Top 10 Écoles – Score SAT Total

- **Calcul du score total :**  
  `total_SAT = average_math + average_reading + average_writing`
- **Résultat stocké dans :** `top_10_schools`
- **Colonnes retournées :** `school_name`, `total_SAT`
- **Ordre de tri :** décroissant selon `total_SAT`

📊 _Visualisation :_ Diagramme en barres horizontales des 10 meilleurs scores

---

### 3. 📊 Borough avec Plus Grande Variabilité des Scores SAT

- **Regroupement par :** `borough`
- **Statistiques calculées :**
  - Moyenne du score SAT (`average_SAT`)
  - Écart-type (`std_SAT`)
  - Nombre d'écoles (`num_schools`)
- **Résultat final dans :** `largest_std_dev`  
- **Colonnes retournées :** `borough`, `num_schools`, `average_SAT`, `std_SAT`
- **Toutes les valeurs numériques sont arrondies à 2 décimales**

📉 _Visualisation :_ Boîtes à moustaches par arrondissement (boxplot)

---

## 📊 Graphiques Inclus

Le projet inclut plusieurs visualisations produites avec **Matplotlib** et **Seaborn** :
- Histogrammes de distribution
- Graphiques en barres
- Diagrammes à moustaches (boxplots)
- Représentations comparatives inter-arrondissements

---

## 🛠️ Technologies Utilisées

- 🐍 Python 3
- 📊 Pandas
- 📈 Matplotlib & Seaborn
- 📓 Jupyter Notebook

---

## 🧠 Compétences Développées

- 🔍 Analyse exploratoire des données (EDA)
- 🧼 Nettoyage et transformation de données avec pandas
- 📉 Calculs statistiques : moyenne, somme, écart-type
- 📊 Création de visualisations interprétables

---

## 📁 Organisation du Répertoire

