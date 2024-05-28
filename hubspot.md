
# Documentation API Hubspot - Ici Formation V1
Date de création : 10/04/2024

## Introduction

L'API Ici Formation Hubspot est conçue pour permettre aux clients de recevoir les leads de manière automatisée et en temps réel. Cette documentation vise à expliquer comment intégrer et utiliser l'API POST pour transmettre des leads.
Cette documentation est à destination de l'équipe du client souhaitant réceptionner les leads.

Voici les étapes à suivre :

### 1. Créer une application privée
* Dans votre compte HubSpot, cliquez sur l'icône Paramètres dans la barre de navigation principale.
* Dans le menu latéral de gauche, accédez à Intégrations > Applications privées.
* Cliquez sur Créer une application privée.
* Dans l'onglet Informations de base, configurez les détails de votre application :
- Saisissez le nom de votre application.
- Passez le curseur de la souris sur le logo de variable et cliquez sur l'icône de téléchargement pour télécharger une image carrée qui servira de logo pour votre application.
- Saisissez une description pour votre application.
* Cliquez sur l'onglet Domaines.
* Sélectionnez la case à cocher Écriture ou crm.objects.contacts.write pour chaque domaine auquel vous souhaitez que votre application privée puisse accéder.
* Lorsque vous avez terminé de configurer votre application, cliquez sur Créer une application dans l'angle supérieur droit.
* Dans la boîte de dialogue, vérifiez les informations sur le jeton d'accès de votre application, puis cliquez sur Continuer de créer.

Communiquez nous le jeton d'authentification afin que nous puissions passer des appels à l'API.

### 2. Champs transmis à l'application
Par défaut nous transmettons les informations suivantes :

* Nom
* Prénom
* Téléphone
* Email

Si vous souhaitez recevoir d'autres informations disponibles dans notre formulaire, il faut créer et nous communiquer le nom exact.

Voici les informations supplémentaires que nous pouvons envoyer :
* Nom de la formation
* Préférence de rappel du contact
* Civilité
* Ville


## Support

Pour toute question ou assistance technique, veuillez contacter le support d'Ici Formation à l'adresse tech@iciformation.fr ou a.stoj@iciformation.fr

---
