# 🔬 SkinAI — Détection de Lésions Cutanées par IA

<div align="center">

![SkinAI](https://img.shields.io/badge/SkinAI-Deep%20Learning-00d4ff?style=for-the-badge&logo=python)
![Flask](https://img.shields.io/badge/Flask-2.x-black?style=for-the-badge&logo=flask)
![TensorFlow](https://img.shields.io/badge/TensorFlow-VGG16-FF6F00?style=for-the-badge&logo=tensorflow)
![MySQL](https://img.shields.io/badge/MySQL-XAMPP-4479A1?style=for-the-badge&logo=mysql)

**Application Web Flask intégrant un modèle Deep Learning (VGG16) pour la détection de lésions cutanées malignes ou bénignes.**

</div>

---

## 📌 Description

**SkinAI** est une application Web complète développée en Python (Flask) dans le cadre du module **Introduction à l'IA** — TD8, ENSTAB 2025/2026.

Elle permet aux professionnels de santé de :
- 🔐 Se connecter de manière sécurisée
- 🖼️ Soumettre l'image d'une lésion cutanée
- 🤖 Obtenir une prédiction IA (**Malignant** ou **Benign**) avec taux de confiance
- 📋 Consulter l'historique complet des diagnostics enregistrés

---

## 🖥️ Démonstration

### 🔐 Page de connexion
![Login](screenshots/login.png)

### 📊 Tableau de bord
![Dashboard](screenshots/dashboard.png)

### 🩺 Analyse patient
![Predict](screenshots/predict.png)

### ✅ Résultat du diagnostic
![Result](screenshots/result.png)

### 📋 Historique patients
![Patients](screenshots/patients.png)

---

## 🧠 Modèle IA

| Paramètre | Valeur |
|-----------|--------|
| Architecture | VGG16 (Transfer Learning) |
| Input | Image 224×224 px |
| Output | Probabilité de malignité (0 → 1) |
| Seuil | > 0.5 = **Malignant** / ≤ 0.5 = **Benign** |
| Dataset | Skin Cancer: Malignant vs Benign (Kaggle) |

> ⚠️ Le fichier modèle `vgg16_malignant_vs_benign.h5` (~130MB) n'est pas inclus dans ce repo (limite GitHub 100MB). À placer manuellement dans le dossier `model/`.

---

## 🛠️ Technologies utilisées

| Catégorie | Outil |
|-----------|-------|
| Backend | Python 3.x, Flask |
| IA / ML | TensorFlow, Keras, VGG16 |
| Base de données | MySQL via XAMPP |
| Frontend | HTML5, Bootstrap 5, CSS3 |
| Polices | Syne, DM Sans (Google Fonts) |

---

## 📁 Structure du projet

```
SKIN_CANCER_APP2/
├── model/
│   └── vgg16_malignant_vs_benign.h5   ← (à ajouter manuellement)
├── static/
│   ├── uploads/                        ← images soumises par les utilisateurs
│   └── style.css                       ← design dark theme
├── templates/
│   ├── login.html                      ← page de connexion
│   ├── dashboard.html                  ← tableau de bord
│   ├── predict.html                    ← formulaire d'analyse
│   ├── result.html                     ← affichage du résultat
│   └── patients.html                   ← historique des diagnostics
├── app.py                              ← logique Flask principale
├── database.sql                        ← script de création BDD
└── README.md
```

---

## ⚙️ Installation

### 1. Cloner le repo
```bash
git clone https://github.com/just-a-useless-web/skin-cancer-detector.git
cd skin-cancer-detector
```

### 2. Installer les dépendances Python
```bash
pip install flask tensorflow numpy mysql-connector-python
```

### 3. Configurer la base de données
- Démarrer **XAMPP** → Apache + MySQL
- Ouvrir `http://localhost/phpmyadmin`
- Onglet **SQL** → coller le contenu de `database.sql` → **Exécuter**

### 4. Placer le modèle
Copier `vgg16_malignant_vs_benign.h5` dans le dossier `model/`

### 5. Lancer l'application
```bash
python app.py
```
Ouvrir dans le navigateur : `http://localhost:5000`

---

## 🔐 Identifiants par défaut

| Champ | Valeur |
|-------|--------|
| Utilisateur | `admin` |
| Mot de passe | `1234` |

---

## 🚀 Fonctionnalités

| Route | Description |
|-------|-------------|
| `/` | Page de connexion sécurisée |
| `/dashboard` | Tableau de bord principal |
| `/predict` | Formulaire d'analyse IA |
| `/patients` | Historique des diagnostics (tri par date) |
| `/logout` | Déconnexion et vidage de session |

---

## 👩‍💻 Auteure

**Lina Zammel** — 1ère année ingénieur, Technologies Avancées (1TA)  
ENSTAB — École Nationale des Sciences et Technologies Avancées de Borj Cédria  
Université de Carthage — 2025/2026  

Enseignante : **Amira Echtioui**

