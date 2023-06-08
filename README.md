# CSGames-Croesus-Stocks-2023

## Contexte
Les fondateurs d'Atlantis ont besoin de lever du capital pour financer la construction de leur ville sous-marine. 
Pour ce faire, ils décident d'investir 1 000 000$ dans le marché boursier.
De plus, ils ont la chance d'avoir en leur possession un oracle qui leur permet de voir le prix des actions des entreprises jusqu'à un mois dans le futur! 

## Description
Votre challenge est d’écrire un programme qui va proposer des transactions boursières à faire sur une période de temps prédéterminée afin de maximiser le profit sur un investissement initial. La période de temps proposée est entièrement dans le passé.

Vous serez évalué sur le montant de profit total généré par votre séquence de transactions, ainsi que par la structure, le style et la créativité de votre code, que vous devrez soumettre à la fin du challenge.

Vous pouvez utiliser le langage de programmartion de votre choix pour faire ce challenge. 

### Input
Les intrants à votre programme seront les paramètres d’une simulation boursière:
- Une liste de symboles boursiers à laquelle votre investissement devra se limiter:
  - Par exemple 'GM' et 'F' sont les symboles boursiers pour General Motors et Ford respectivement.
- Une date de début
  - Par exemple 2023/01/01
- Une date de fin
  - Par exemple 2023/02/01
- Un montant initial à investir
  - Par exemple $1000000

### Output
Votre programme devra produire une liste de transactions en JSON que vous devrez soummetre à une API de validation pour en assurer la conformité et obtenir la valeur totale finale de votre investissement. Voir [API_SPECS.md](./API_SPECS.md) pour plus de détails.

### Règles
Les règles du challenge sont les suivantes:
- Vous pouvez exécuter au maximum une transaction par jour ;
- Vous ne pouvez détenir qu'un seul titre à la fois ("all in"):
  - Donc en tout temps, tout l'argent doit être en votre possession en comptant ou investi dans un des titres permis pour la simulation en cours ;
- La quantité d'actions détenue n'est pas limitée à être une valeur entière:
  - Par exemple, si le prix de l'action GM est de $39.31, vous pouvez en acheter une quantité de 25438.8196388 ;
- Il n'est pas permis de faire des transactions pendant les weekends ou des jours fériés.
- Le prix utilisé pour les calculs sera le prix “Open”

### Stratégie
Quelques idées:
- Si vous ne faites pas de transactions, vous êtes certains de ne pas perdre d’argent!
- Vous pouvez utiliser une stratégie arbitraire:
  - Le premier jour, commencer par acheter un titre au hasard 
  - Pour chaque jour, décider arbitrairement de le conserver ou de l’échanger contre un autre
  - Au dernier jour, vendre le titre détenu
- Essayer de voir “dans le futur” (toujours à l’intérieur des dates de début et de fin) si le prix d’un titre augmente ou baisse afin de décider de de l’acheter ou le vendre

Les moyens à utiliser pour obtenir les prix des titres dans le passé (ou toute autre information que vous jugez pertinente) sont à votre discrétion. L’API Yahoo! Finance est une bonne place pour commencer, et ce sera la source de prix officielle qui sera utilisée pour calculer les profits de chaque équipe à la fin du challenge.

**Note: Il est interdit de consulter une base de données client pour obtenir les prix des titres**

## Déroulement
Le premier 2h30 du challenge se fera en mode test. Ensuite, 30 minutes avant la fin du challenge, les paramètres de la simulation finale vous seront communiqués.

### Simulation de test
Paramètres de la simulation de test: [TEST_SIM.md](./TEST_SIM.md)

### Simulation finale
Paramètres de la simulation finale: [FINAL_SIM.md](./FINAL_SIM.md)

### API de validation
Détails pour l'API de validation: [API_SPECS.md](./API_SPECS.md)

## Soumission
Avant la fin du challenge vous devrez:
- Soumettre votre résultat pour le challenge de test à l‘API de validation
  - Seule votre dernière soumission sera retenue
- Soumettre votre résultat pour le challenge final à l‘API de validation
  - Seule votre dernière soumission sera retenue

## Communication
Durant le déroulement de la compétition les réprésentants de Croesus seront disponibles pour répondre à vos questions en salle ou via le salon "Hackathon - Atlantide en Action".
De plus, le salon Google Meet "Hackathon - Atlantide en Action - Live Profits" a été créé pour afficher en direct le résultats des participants!

### Rejoindre les Google Meet
* Général: https://chat.google.com/room/AAAAhG-jqeY?cls=7
* Live Results: https://chat.google.com/room/AAAAV7TSLFc?cls=7
