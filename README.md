# PriseRFID-v1

## Description
Prise de courant contrôlable par carte et badge RFID. 
version basé sur Arduino nano pour tester le principe.
![priseRFID exterieur](/images/DSC09147.JPG)
![priseRFID interieur](/images/DSC09144.JPG)

## Fonctions 
* Alimenter la prise en fonction des autorisations associées à la carte
* Associer différent temps d’accès à l’électricité en fonction des puces (nécessite une puce RTC)

## Composants
* Adruino Nano
* Relai 5v 
* Transformateur 220v AC - 5V DC
* 3 LEDs
* 3 résistances
* Module RFID RC 522
* Prise électrique murale
* Rallonge électrique
* Cables électriques pour 220v-15A

## Schéma d'assemblage électronique
![schéma assemblage](/images/PriseRFIDNano.png)

## Boitier
* MDF 3 mm

## Echanges d'informations
Ce prototype n’échange pas d’information avec d’autre système. Les numéros de puce RFID sont codés « en dur » dans le programme.

### Fonctionnement
La personne présente la carte devant la zone du capteur, si elle est reconnue mais ne fait pas parti des cartes/ puce qui autorise l’accès, un LED rouge s’allume. Si au contraire la carte autorise l’accès, une LED verte s’allume et le relai se déclenche. Pour arrêter le déclenchement du relai, il suffit de passer de nouveau la carte devant le lecteur. 

## To do
* Décompte du temps de connexion associé aux différentes puces (ajouter une puce RTC)
* Désactivation de la prise uniquement avec la puce RFID qui a été utilisé pour l’activer 
