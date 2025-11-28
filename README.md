# 📊 Patient Risk Healthcare Dashboard

Ce projet présente un tableau de bord interactif réalisé dans **Tableau Desktop** pour analyser les risques de santé des patients.  
L’objectif est avant tout l’apprentissage de Tableau pour débutants.

---

## 🩺 Contexte du projet

Une clinique souhaite suivre l’état de santé de ses patients afin d’identifier ceux présentant un risque cardiovasculaire élevé.  
Le dashboard permet de visualiser les KPIs de santé, la répartition démographique et les indicateurs liés au risque cardio.

---

## 🎯 Objectifs

- Reproduire un tableau de bord donné
- Créer des visualisations simples
- Organiser et mettre en forme un dashboard lisible
- Apprendre les conteneurs et l’ergonomie dans Tableau

---

## 📌 Indicateurs (KPIs)

### Principaux
- Total Patients
- Âge moyen
- Répartition par Genre

### Bonus
- % Fumeurs
- % Consommateurs d’alcool
- % Actifs en sport
- Tension artérielle moyenne
- Cholestérol moyen
- Glucose moyen
- Score de risque cardiovasculaire

---

## 🔍 Dataset

Dataset : **Cardiovascular Disease Dataset**  
Format : CSV  
Colonnes utilisées :
`id, age, gender, height, weight, ap_hi, ap_lo, cholesterol, gluc, smoke, alco, active, cardio`

---

## 🧹 Préparation des données

⚠️ Le dataset a été utilisé **sans nettoyage** :  
Aucune suppression d’anomalies ou modification des valeurs.

Objectif du projet → focus sur l’apprentissage de Tableau, pas sur la data cleaning.

Des améliorations futures peuvent inclure :
- Correction des tensions artérielles aberrantes
- Ajout IMC (BMI)
- Normalisation des indicateurs santé
- Suppression de valeurs extrêmes

---

## 🧮 Champs calculés dans Tableau

| Champ | Formule |
|------|---------|
| Age_en_annee | `INT([age] / 365.25)` |
| Tranche_Age | Groupes : `<30`, `30-39`, `40-49`, `50+` |
| HighBP | `[ap_hi] >= 140 OR [ap_lo] >= 90` |
| RiskScore | `[cholesterol] + [gluc] + (IF [HighBP] THEN 1 ELSE 0 END)` |

---

## 📈 Visualisations incluses

- KPI cards (Total Patients, Age, Smoke %, Active %...)
- Donut Chart : Répartition par genre
- Bar Charts : Tranche d’âge, Cholestérol, Glucose, Tension
- RiskScore par genre et âge

---

## 🖥️ Dashboard

Aperçu du tableau de bord :

<img width="1593" height="797" alt="tableau-dashboard" src="https://github.com/user-attachments/assets/371c16ae-d0ce-4c58-8117-c53a272a6eb8" />

