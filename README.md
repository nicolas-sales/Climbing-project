# Climbing Hold Detection & Color Analysis with YOLOv8

Ce projet utilise YOLOv8 pour détecter automatiquement les prises d’escalade sur des murs artificiels, puis analyse leur couleur dominante afin d’identifier visuellement les différentes voies.


---

## Objectifs

- Détection automatique des prises d’escalade sur photo.

- Identification de la couleur dominante de chaque prise via KMeans.

- Regroupement des prises par couleur pour reconstituer des voies.

- Base pour une future estimation automatique de la cotation.

---

## Technologies

- Python 3.10+

- Ultralytics YOLOv8

- OpenCV

- NumPy, Matplotlib

- CUDA (optionnel, pour accélération GPU)

---

## Structure du projet

Climbing project/
├── train/
│   ├── images/         # Images d'entraînement
│   └── labels/         # Fichiers YOLO .txt (bounding boxes)
├── valid/
│   ├── images/         # Images de validation
│   └── labels/
├── test/
│   └── images/         # Images à tester (prises inconnues)
├── data.yaml           # Fichier de configuration YOLO
├── runs/               # Résultats de l'entraînement YOLOv8
│   └── detect/train/   # Dossier de sortie par défaut
│       └── results.png # Graphiques d'entraînement
├── best.pt             # Modèle YOLOv8 entraîné
├── notebooks/
│   └── Climbing project.ipynb  # Notebook principal


 ## Résultat d'entraînement YOLOv8

Voici l’évolution des performances de détection pendant l'entraînement :

![Courbes d'entraînement YOLOv8](runs/detect/train/results.png)
 
 
 