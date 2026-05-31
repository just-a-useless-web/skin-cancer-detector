# SKIN_CANCER_APP — Guide d'installation

## Prérequis
- Python 3.x
- XAMPP (MySQL)
- pip : Flask, tensorflow, numpy, mysql-connector-python

## Installation

### 1. Installer les dépendances
```bash
pip install flask tensorflow numpy mysql-connector-python
```

### 2. Base de données
- Démarrer XAMPP → MySQL
- Ouvrir phpMyAdmin ou MySQL Workbench
- Exécuter `database.sql`

### 3. Placer le modèle
Copier `vgg16_skin_cancer.h5` dans le dossier `model/`

### 4. Structure du projet
```
SKIN_CANCER_APP/
├── model/
│   └── vgg16_skin_cancer.h5
├── static/
│   ├── uploads/
│   └── style.css
├── templates/
│   ├── login.html
│   ├── dashboard.html
│   ├── predict.html
│   ├── result.html
│   └── patients.html
├── app.py
└── database.sql
```

### 5. Lancer l'application
```bash
python app.py
```
Ouvrir : http://localhost:5000

**Login par défaut :** admin / 1234
