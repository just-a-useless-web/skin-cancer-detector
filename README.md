# 🔬 SkinAI — Détection de Lésions Cutanées par IA

<div align="center">

![SkinAI](https://img.shields.io/badge/SkinAI-Deep%20Learning-00d4ff?style=for-the-badge&logo=python)
![Flask](https://img.shields.io/badge/Flask-2.x-black?style=for-the-badge&logo=flask)
![TensorFlow](https://img.shields.io/badge/TensorFlow-VGG16-FF6F00?style=for-the-badge&logo=tensorflow)
![MySQL](https://img.shields.io/badge/MySQL-XAMPP-4479A1?style=for-the-badge&logo=mysql)

**Application Web Flask intégrant un modèle Deep Learning (VGG16) pour la détection de lésions cutanées malignes ou bénignes.**

*Module : Introduction à l'IA — TD8 | ENSTAB 2025/2026 | Enseignante : Amira Echtioui*

</div>

---

## 🖥️ Aperçu de l'application

### 🔐 1. Connexion
Accéder à l'application avec les identifiants sécurisés.

![Login](screenshots/Screenshot_2026-05-31_150427.png)

---

### 📊 2. Tableau de bord
Trois actions disponibles : Nouvelle analyse, Historique patients, Déconnexion.

![Dashboard](screenshots/Screenshot_2026-05-31_150552.png)

---

### 🩺 3. Soumettre une analyse
Renseigner le nom du patient, l'âge, et uploader une image de la lésion cutanée.

![Predict](screenshots/Screenshot_2026-05-31_150646.png)

---

### ✅ 4. Résultat du diagnostic IA
Le modèle VGG16 analyse l'image et retourne un diagnostic **Malignant** ou **Benign** avec un taux de confiance et une barre de progression.

![Result](screenshots/Screenshot_2026-05-31_150848.png)

---

### 📋 5. Historique patients
Consulter tous les diagnostics enregistrés avec les images, résultats et dates.

![Patients](screenshots/Screenshot_2026-05-31_151002.png)

---

## 🔐 Identifiants

| Champ | Valeur |
|-------|--------|
| Utilisateur | `admin` |
| Mot de passe | `1234` |

---

## 🧠 Comment fonctionne l'IA ?

| Étape | Description |
|-------|-------------|
| 1 | L'image est redimensionnée en **224×224 px** |
| 2 | Normalisée (valeurs entre 0 et 1) |
| 3 | Analysée par le modèle **VGG16** |
| 4 | Score > 0.5 → **Malignant** / Score ≤ 0.5 → **Benign** |
| 5 | Résultat + probabilité sauvegardés en base de données |

> ⚠️ Ce diagnostic est une **aide à la décision**. Il ne remplace pas un dermatologue.

---

## 👩‍💻 Auteure

**Lina Zammel** — 1ère année ingénieur Technologies Avancées (1TA)  
ENSTAB — Université de Carthage — 2025/2026
