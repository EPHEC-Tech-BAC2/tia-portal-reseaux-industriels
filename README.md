# Réseaux industriels — TIA Portal (2AU)

Travaux pratiques réalisés à l'EPHEC-Tech (2AU, 2025-2026), à trois : **EL YAZAMI Yassine**, **ELMURZAEV Ibrahim**, **BALDE Alpha Ibrahima**.

## Le cours

Ce dépôt regroupe les travaux pratiques du cours de communication réseaux, dont l'objectif est d'apprendre à mettre en réseau des équipements d'automatisation (automates, variateurs, écrans HMI) et à programmer leur communication sous **TIA Portal**.

## TP1 — Communication entre deux automates (TSEND/TRCV)

Mise en place d'une communication point à point entre deux automates S7-1200 à l'aide des blocs **TSEND** et **TRCV**. Le premier automate envoie un ordre à distance au second, qui pilote une LED en fonction de l'ordre reçu. Ce TP permet de comprendre l'échange de données non cyclique entre deux CPU sur un même réseau Ethernet.

## TP2 — Communication automate / variateur / HMI via PROFINET

Mise en œuvre d'une architecture PROFINET complète reliant un automate SIEMENS CPU 1215C, un variateur de fréquence G120 (CU250S-2 PN) et un écran HMI KTP700 Basic via un switch SCALANCE XB005.

- Configuration réseau (adresses IP, noms PROFINET, télégramme standard 1)
- Programmation du bloc fonctionnel **SINA_SPEED** (bibliothèque DriveLib) pour piloter le variateur
- Création d'un Data Block structuré (`DB_HMI`) servant d'interface entre le programme PLC et l'écran HMI
- Paramétrage de l'IHM : consigne de vitesse, bargraphe de vitesse réelle, voyants d'état, boutons Execute/Halt/AckFlt
- Tests validés : démarrage à 1000 RPM, arrêt, acquittement de défaut

## Logiciel

- TIA Portal V20 (Siemens)

## Contenu du dépôt

- `tp1-tsend-trcv-led-distance/` : projet TIA Portal du TP1
- `tp2-sina-speed-hmi-profinet/` : projet TIA Portal du TP2
- `rapport/` : rapports du TP2