# 🏫 Analyse des Résultats du SAT dans les Lycées Publics de New York City

![New York City schoolbus](schoolbus.jpg)  
*Photo by [Jannis Lucas](https://unsplash.com/@jannis_lucas) on [Unsplash](https://unsplash.com)*

---

## 📘 Contexte

Les **SATs** sont des tests standardisés utilisés aux États-Unis pour évaluer les compétences des élèves en **lecture**, **mathématiques**, et **écriture**. Chaque section est notée sur **800 points**, pour un total maximal de **2400**.  
Ces scores sont déterminants pour l’admission universitaire, et leur analyse permet d’évaluer la qualité des établissements scolaires.

Ce projet vise à répondre à **trois questions majeures** concernant les écoles publiques de **New York City (NYC)** à l’aide des données fournies dans le fichier `schools.csv`.

---

## 🎯 Objectifs du Projet

1. **Identifier les écoles ayant les meilleurs résultats en mathématiques**
2. **Lister les 10 meilleures écoles selon le score SAT total**
3. **Déterminer l’arrondissement avec la plus forte dispersion des scores SAT**

---

## 🧰 Données

Le fichier **`schools.csv`** contient les colonnes suivantes :

| Colonne           | Description                                |
|-------------------|--------------------------------------------|
| `school_name`     | Nom de l’établissement                     |
| `borough`         | Arrondissement de NYC                      |
| `average_math`    | Score moyen en mathématiques               |
| `average_reading` | Score moyen en lecture                     |
| `average_writing` | Score moyen en écriture                    |

---

## 📊 Analyses Réalisées

### ✅ 1. Écoles les plus performantes en mathématiques
- Critère : score moyen en math ≥ 640 (soit 80 % de 800)
- Résultat enregistré dans un DataFrame `best_math_schools`
- Colonnes : `school_name`, `average_math`
- Tri décroissant selon `average_math`

### ✅ 2. Top 10 des écoles selon le score SAT combiné
- Score total = `average_math` + `average_reading` + `average_writing`
- Résultat enregistré dans un DataFrame `top_10_schools`
- Colonnes : `school_name`, `total_SAT`
- Tri décroissant selon `total_SAT`

### ✅ 3. Arrondissement avec la plus grande variabilité de scores
- Calcul de l’écart type (`std_SAT`) du score total pour chaque `borough`
- Résultat dans un DataFrame `largest_std_dev`
- Colonnes : `borough`, `num_schools`, `average_SAT`, `std_SAT`
- Toutes les valeurs numériques sont arrondies à **2 décimales**

---

## 🛠️ Compétences Développées

- 🔍 Analyse exploratoire des données (EDA)
- 🧼 Nettoyage et transformation de données avec **pandas**
- 📉 Calculs statistiques simples : moyenne, somme, écart-type
- 📊 Visualisation potentielle avec matplotlib/seaborn (en option)

---

## 📁 Organisation du Répertoire

