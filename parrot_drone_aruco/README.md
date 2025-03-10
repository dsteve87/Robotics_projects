# Drone Navigation with Aruco Marker and PID Control

Ce projet permet à un drone de naviguer automatiquement en utilisant un marqueur Aruco comme référence. Il utilise un contrôle PID (Proportional-Integral-Derivative) pour ajuster la position du drone en fonction de l'erreur détectée par la caméra et du marqueur. Le drone prend en compte les erreurs de position horizontale, verticale, et de distance pour se déplacer.

## Fonctionnalités
- Détection de marqueurs Aruco en temps réel.
- Calcul de l'erreur de position du drone par rapport au marqueur Aruco.
- Utilisation d'un contrôle PID pour ajuster la position du drone horizontalement, verticalement, et en fonction de la distance.
- Prise en charge de la caméra du drone pour la détection de marqueurs et l'affichage en direct de l'image.
- Connexion avec un drone via l'API `ps_drone`.
- Affichage de la batterie du drone.

## Prérequis
Avant d'exécuter ce projet, assurez-vous d'avoir les éléments suivants installés et configurés :
- **Python 3** 
- **Bibliothèques nécessaires** :
  - OpenCV
  - numpy
  - ps_drone
  - cv2 (pour la capture vidéo et la détection Aruco)

Pour installer les bibliothèques nécessaires, exécutez les commandes suivantes :
```bash
pip install opencv-python numpy
```

