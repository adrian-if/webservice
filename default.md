# Documentation API - Ici Formation V2.1
Date de création : 10/04/2024

Date de dernière modification : 28/11/2024

## Vue d'ensemble

L'API Ici Formation permet de recevoir automatiquement et en temps réel les informations de vos prospects (leads). Cette documentation vous guidera pas à pas dans son intégration.

Si vous n'avez pas la possibilité de créer une url de réception vous pouvez utiliser un service tiers comme Zapier ou le CRM Hubspot.

## Fonctionnement

1. Un prospect remplit un formulaire sur iciformation.fr
2. Notre système vérifie si vous avez configuré une API
3. Les informations du prospect sont envoyées instantanément à votre système

## Étapes de mise en place
- Configurer votre endpoint de réception
- Nous communiquer vos informations d'authentification
- Effectuer un test avec notre équipe
- Vérifier la réception des données

## Options d'intégrations

### Pour les équipes techniques
- Intégration directe via API REST

### Pour les non-développeurs
- Intégration via Zapier (sans code)
- Création d'un webhook dans votre CRM
- Connexion directe via Hubspot avec documentation disponible ici : https://github.com/adrian-if/webservice/blob/main/hubspot.md

La plupart des CRM modernes permettent de créer facilement des webhooks.
Le but est de créer une url de réception qui pourra récupérer les données (voir exemple de payload) via une requête POST.

## Structure des données

Les données sont envoyées au format JSON avec la structure suivante :

| Champ | Description | Exemple |
|-------|-------------|---------|
| nom | Nom du prospect | Doe |
| prenom | Prénom du prospect | John |
| civilite | Civilité | M. |
| tel | Numéro de téléphone | 0102030405 |
| email | Adresse email | john.doe@example.com |
| ville | Ville (en minuscules) | paris |
| code_postal | Code postal | 75001 |
| formation | Formation d'intérêt | Développement Web |
| horaire_rappel | Moment préféré pour le contact | après-midi |
| statut | État du prospect | prospect |
| client | Nom de votre société | XYZ Formations |
| id_client | Votre identifiant unique | 1234 |

## Exemple de payload

{
  "nom": "Doe",
  "prenom": "John",
  "civilite": "M.",
  "tel": "0102030405",
  "email": "john.doe@example.com",
  "ville": "paris",
  "code_postal": "75001",
  "statut": "prospect",
  "horaire_rappel": "après-midi",
  "formation": "Développement Web",
  "client": "XYZ Formations",
  "id_client": "1234"
}

## Sécurité

Afin de garantir la sécurité de votre API nous conseillons de mettre en place une authorization par Bearer Token, API Key, Token ou X Token.
Par la suite vous pouvez nous communiquer l'authentification.

## Traitement des Réponses

### Réussite

En cas de succès, l'API renvoie un statut HTTP 200 avec un corps de réponse vide.

## Support

Pour toute question ou assistance technique, veuillez contacter le support d'Ici Formation à l'adresse tech@iciformation.fr ou a.stoj@iciformation.fr

---
