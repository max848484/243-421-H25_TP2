# TP2 Interface CCP

## Matériel
- 1 Carte PIC
- 1 Accéléromètre ADXL202
- 1 Servomoteur HS-422
- 1 Afficheur LCD série

## Partie A: Contrôle d’une serrure mécanique

### Préparation
- Lecture de la fiche technique du HS-422.
- Sélectionner les valeurs de départ des registres nécessaires au bon fonctionnement du module PWM (PR2, fosc, Valeur prescale, 10 bits – CCPR4L:CCP4CON<5:4>).

### Manipulations

1. Monter le servomoteur HS-422 sur la broche C2 du PIC

![image](https://github.com/max848484/243-421-H24_TP2/assets/156249332/dbf11276-4e27-4197-a139-a13d9e8ca8dc)


2. Écrire un programme qui demande à un utilisateur, via l’application de terminal TERA TERM, s’il veut barrer (‘L’) ou débarrer (‘U’) la porte et règle la position du servomoteur pour barrer ou pour débarrer. 

3. Au démarrage, le moteur doit se mettre à la position neutre.
Si l’utilisateur demande de débarrer, le moteur se déplace jusqu’à la position moins 90 degrés.
Si l’utilisateur demande de barrer, le moteur se déplace jusqu’à la position plus 90 degrés.

## Partie B : Mesure de l’accélération

### Préparation
- Lecture de la fiche technique du ADXL202
- Schéma de branchement (PIC, ADXL et potentiomètre)
- Sélectionner les valeurs de départ des registres nécessaires au bon fonctionnement du module input capture.

### Manipulations

1- Monter l’accéléromètre et le LCD sur le PIC
L’ADXL202 est monté sur une mini-carte :

![image](https://github.com/max848484/243-421-H24_TP2/assets/156249332/0b387d02-620c-468e-b7bc-d1a52b631311)

Installer cette carte en plaçant :
- Alimentation = 5 V et un condensateur de découplage de 0,1 µF
- Rset = 125 kΩ
- Cx et Cy = 0, 01 µF

2- Écrire un programme sur le PIC qui affiche la durée de pulse haute, la période et l’accélération pour chacun des 2 axes, sur l’écran LCD.

## Évaluation
### Faire vérifier
- Le fonctionnement sera vérifié au laboratoire.

### Remettre
- Les programmes des deux parties bien commentées.
- Un fichier de documentation qui explique les paramètres configurés pour les modules CCP. 
Les valeurs doivent être justifiées à l’aide de calculs.


