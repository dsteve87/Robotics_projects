Drone Navigation with Aruco Marker and PID Control
Ce projet permet à un drone de naviguer automatiquement en utilisant un marqueur Aruco comme référence. Il utilise un contrôle PID (Proportional-Integral-Derivative) pour ajuster la position du drone en fonction de l'erreur détectée par la caméra et du marqueur. Le drone prend en compte les erreurs de position horizontale, verticale, et de distance pour se déplacer.

Fonctionnalités
Détection de marqueurs Aruco en temps réel.
Calcul de l'erreur de position du drone par rapport au marqueur Aruco.
Utilisation d'un contrôle PID pour ajuster la position du drone horizontalement, verticalement, et en fonction de la distance.
Prise en charge de la caméra du drone pour la détection de marqueurs et l'affichage en direct de l'image.
Connexion avec un drone via l'API ps_drone.
Affichage de la batterie du drone.
Prérequis
Avant d'exécuter ce projet, assurez-vous d'avoir les éléments suivants installés et configurés :

Python 3.x : Le projet a été développé avec Python 3.
Bibliothèques nécessaires :
OpenCV
numpy
ps_drone
cv2 (pour la capture vidéo et la détection Aruco)
Pour installer les bibliothèques nécessaires, exécutez les commandes suivantes :

bash
Copier
Modifier
pip install opencv-python numpy
Installation
Clonez le projet depuis GitHub :

bash
Copier
Modifier
git clone https://github.com/username/projet-drone-aruco.git
cd projet-drone-aruco
Téléchargez les fichiers de calibration : Le projet utilise des fichiers de calibration pour la caméra (cal_vals/ret.npy, cal_vals/mtx.npy, cal_vals/dist.npy). Vous pouvez les obtenir à partir de votre propre processus de calibration ou utiliser des fichiers de calibration génériques.

Exécutez le script : Une fois que vous avez tout configuré, vous pouvez exécuter le script Python principal.

bash
Copier
Modifier
python main.py
Utilisation
Lancez le script et le drone commencera à voler.
Le système détectera les marqueurs Aruco, et le drone ajustera sa position en fonction de l'erreur détectée.
Vous pouvez quitter le programme à tout moment en appuyant sur la touche q lorsque la fenêtre OpenCV est active.
Contrôle PID
Le contrôle PID est utilisé pour ajuster le mouvement du drone dans trois directions :

Position horizontale : Si le marqueur Aruco est trop à gauche ou à droite de l'image, le drone ajustera sa position horizontalement.
Position verticale : Si le marqueur est trop haut ou trop bas, le drone ajustera sa hauteur.
Distance : Si le marqueur est trop proche ou trop éloigné, le drone se déplacera en avant ou en arrière.
Architecture du Code
Initialisation du Drone :

Connexion au drone via ps_drone.Drone().
Prise en charge de la caméra du drone pour capturer des images en temps réel.
Calibration de la caméra :

Chargement des paramètres de calibration de la caméra pour compenser les distorsions optiques.
Détection du Marqueur Aruco :

Détection en temps réel des marqueurs Aruco via OpenCV et estimation de leur position dans l'espace.
Utilisation des coordonnées du marqueur pour calculer l'erreur par rapport à la position souhaitée du drone.
Contrôle PID :

Utilisation des paramètres PID pour ajuster la vitesse du drone dans les directions horizontale, verticale et en fonction de la distance.
Affichage :

Visualisation en temps réel de l'image avec les marqueurs détectés et les ajustements du drone.
Exemples de commandes
Décoller : Lorsque le script est exécuté, le drone décolle automatiquement après 10 secondes.
Atterrissage : Le drone atterrit automatiquement à la fin du programme ou en cas de perte de la détection du marqueur.
Auteurs
Votre nom – Développeur principal
Collaborateurs – Liste des contributeurs (le cas échéant)
License
Ce projet est sous licence MIT – voir le fichier LICENSE pour plus de détails.

Remarques
Sécurité : Assurez-vous d'effectuer les tests dans un environnement sécurisé, car le drone pourrait effectuer des mouvements brusques pendant le fonctionnement du programme.
Calibration : Les performances du système de détection peuvent varier en fonction de la précision de la calibration de la caméra.


