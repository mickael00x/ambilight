# Ambilight  
[+ d'exemples](#resultat)
![github image](https://lh3.googleusercontent.com/pw/AM-JKLXWhA97hn9D-qbwrkPP0hHfKKH7MadzGFNt8cdrHaS9_OEa74gNvU6piaQ-k63bs65wTl4br35Hr32-J34S89FlrI_P4saTFCKz_5FsCSrShXqFstYUkIMzzmhYh6k8mrPryWUkY1uAcvSVKFxxLavN=w1718-h1289-no?authuser=0)
### Tutoriel perso inspirée de : https://blog.gamerstuff.fr/tuto-ambilight-diy/


## General info
Ce repo me sert de sauvegarde pour ce projet DYI. Je ne m'attribue aucun des mérites du tutoriel ci-dessus, je n'en fais que la promotion, entre autre.
Si vous avez des questions sur la réalisation, n'hésitez pas à me contacter à le contacter directement, merci :)

## Table of contents

* [Pièces nécessaires](#pieces)
* [Setup](#setup)
* [Installation de Prismatik](#installation)
* [Resultat final](#resultat)

## Pieces
* LED addressable : https://www.amazon.fr/gp/product/B01CDTEJBG/ref=ppx_yo_dt_b_asin_title_o07_s01?ie=UTF8&th=1
* Arduino nano : https://www.amazon.fr/gp/product/B0722YYBSS/ref=ppx_yo_dt_b_asin_title_o07_s01?ie=UTF8&psc=1
* Cable USB 2.0 A vers Mini USB : https://www.amazon.fr/gp/product/B006ZZ1C4M?ie=UTF8&linkCode=sl1&tag=sparrowmake07-21&linkId=a0f7da9028ccd326710e3655a26a3a9c&language=fr_FR&ref_=as_li_ss_tl&th=1
* Alimentation 5v 50w : https://www.amazon.fr/gp/product/B07YVBHH6K/ref=ppx_yo_dt_b_asin_title_o07_s01?ie=UTF8&th=1 <br>
NB : un calcul est nécessaire au niveau de l'alimentation, il faut compter environ 0,3W par LED, pour ma part cela fait donc 0,3 * 136 leds au total. 
* [optionnel] Pièce en 3D : https://www.thingiverse.com/thing:4793999<br>
* [optionnel] Gaines thermorétractable : https://www.amazon.fr/gp/product/B07YS5269R/ref=ppx_yo_dt_b_asin_title_o07_s00?ie=UTF8&psc=1
* [optionnel] Fils electrique cal 22 AWG : https://www.amazon.fr/gp/product/B07G72DRKC/ref=ppx_yo_dt_b_asin_title_o07_s01?ie=UTF8&th=1


## Setup

Download de la bibliothèque Adalight :
```bash 
https://github.com/Wifsimster/adalight_ws2812
```

1. Modifier la variable NUM_LEDS (j'ai opté pour 48 en haut/en bas et 20 sur les côtés, soit un total de 136)
```bash 
 #define NUM_LEDS 136
```

2. Modifier la variable DATA_PIN (le GPIO sur lequel vous avez branché l'installation, dans le cas du tutoriel c'est le 5, mais j'ai choisi le 6) 
```bash 
 #define NUM_LEDS #define DATA_PIN 6
```

## Installation
1. Sur le premier écran cliquez sur Next, puis choisissez « Adalight »<br>
![github image](https://i0.wp.com/blog.gamerstuff.fr/wp-content/uploads/2020/01/tuto-ambilight-diy-07.jpg?w=446&h=250&ssl=1)
2. Saissisez le serial port (l'USB sur lequel l'ardiuno est branché), le baudrate (laissez celui par défaut) et enfin le RGB
![github image](https://i0.wp.com/blog.gamerstuff.fr/wp-content/uploads/2020/01/tuto-ambilight-diy-13.jpg?resize=800%2C331&ssl=1)
3. Saissisez les paramètres qui vous conviennent 
* Number of lEDS : indiquez le nombre de LED de votre installation
* Top : Le nombre de LED sur le haut de l’écran
* Sides : Le nombre de LED sur chacun des côtés de l’écran
* Bottom : Le nombre de LED sur le bas de l’écran
* Thickness : Si vous souhaitez épaissir ou réduire les cases
* Stand Width : Si vous n’avez pas de « trou » de LED sur le ruban du bas mettez 0%
* Invert Oreder : A cocher si le sens n’est pas le bon
* Start Offset : Modifier le chiffre si la LED numéro 1 est mal placée (dans mon cas la 1ere LED n’est pas centrée j’ai donc dû la décaler de 5)

4. ET enfin pour la white balance, je vous conseille R 100, G 66% et B 33%. La LED est très "bleuée" de base.

## Resultat
![github image](https://lh3.googleusercontent.com/pw/AM-JKLXWhA97hn9D-qbwrkPP0hHfKKH7MadzGFNt8cdrHaS9_OEa74gNvU6piaQ-k63bs65wTl4br35Hr32-J34S89FlrI_P4saTFCKz_5FsCSrShXqFstYUkIMzzmhYh6k8mrPryWUkY1uAcvSVKFxxLavN=w1718-h1289-no?authuser=0)
![github image](https://lh3.googleusercontent.com/pw/AM-JKLXCMNea_R9CYxPmJ90UE6ai-W_Ns_fyES0gnyjhrJ4NoHTJ9_qRGy40VjDhZ5MUv8LDNHm3XbfKzfurU4SUh0Cv1q4a3RDLy3lsn_JHC95_-PEQf7LeNgnIMHd-TN1rS0QXDS8RpDSu1UuMWdaVhzYJ=w1718-h1289-no?authuser=0)
![github image](https://lh3.googleusercontent.com/pw/AM-JKLVr31CiKNq4JlBfqEoqHqT1dioX5VnrKLG1i4fMcIm4KH6WRFkp3zOTxm5ohY0b7tvuS17eQXfHkum2MsSJ4y65afpWGjP_kR4mEoT6yH8jQfO34tdZ7-HhkP2m3ZEThx9pFoFFsKhSOS7p3D5S3XZ0=w1718-h1289-no?authuser=0)
