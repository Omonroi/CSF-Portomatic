# CSF-Portomatic
Ce projet est réalisé dans le cadre du module Communication Sans Fil en Licence 1 à l’Université 
Nice Côte D'Azur

Ce projet réalise une porte automatique contrôlée par une carte **UCA (Arduino)**. La porte s'ouvre à 90° via un servomoteur lorsqu'une présence est détectée, et un ruban LED indique l'état du système.

# Fonctionnalités
- **Détection PIR** : Capteur de mouvement infrarouge.
- **Rotor (Servo)** : Ouverture précise à 90 degrés.
- **Indicateur LED** : 
  - **Vert** : Porte fermée / En attente.
  - **Rouge** : Mouvement détecté / Porte ouverte.
- **Temporisation** : La porte reste ouverte 5 secondes avant de se refermer.

#  Branchements

| Composant | Pin Composant | Pin Carte UCA | Servo Motor |
| :--- | :--- | :--- |
| **Servo** 
| Orange (Signal) | **A2** |
| | Rouge (+) | **5V** |
| | Marron (-) | **GND** |
| **PIR** 
| OUT (Signal) | **A3** |
| | VN (Alimentation) | **A5** |
| | GND | **GND** |
| **LEDs** | Data In | **4** |

*Note : La broche A5 fournit le 5V pour le capteur PIR via le code.*

# Bibliothèques
- `Servo` (Standard Arduino)
- `FastLED` (Pour le contrôle du ruban LED)

# Installation
1. Copiez le code du fichier `.ino` dans votre IDE Arduino.
2. Installez la bibliothèque **FastLED** via le gestionnaire de bibliothèques.
3. Branchez les composants selon le tableau ci-dessus.
4. Téléversez !
