
# Documentation API - Ici Formation V2
Date de création : 10/04/2024

## Introduction

L'API Ici Formation est conçue pour permettre aux clients de recevoir les leads de manière automatisée et en temps réel. 
Cette documentation vise à expliquer comment intégrer et utiliser l'API, elle est à destination de l'équipe technique du client souhaitant réceptionner les leads.

Si vous n'avez pas la possibilité de créer une url de réception vous pouvez utiliser un service tiers comme Zapier ou le CRM Hubspot.

Documentation Hubspot : https://github.com/adrian-if/webservice/blob/main/hubspot.md

## Fonctionnement

Lorsque votre centre reçoit un lead sur le site https://www.iciformation.fr/ nous vérifions si une API est en place.
Si oui, nous envoyons une requête POST à votre URL de réception avec les données fournies plus bas.

## Format des données

Les données sont envoyées au format JSON. Voici la structure attendue pour le corps de la requête :

```json
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
```

### Description des champs

- `nom`: Nom du prospect.
- `prenom`: Prénom du prospect.
- `civilite`: Civilité du prospect (ex : M., Mme).
- `tel`: Numéro de téléphone du prospect.
- `email`: Adresse e-mail du prospect.
- `ville`: Ville du prospect (en minuscules).
- `code_postal`: Code postal du prospect.
- `statut`: Statut du prospect (ex : prospect, inscrit).
- `horaire_rappel`: Préférence horaire pour être rappelé.
- `formation`: Titre de la formation recherchée par le prospect.
- `client`: Nom de la société cliente.
- `id_client`: Identifiant unique du client.

## Sécurité

Afin de garantir la sécurité de votre API nous conseillons de mettre en place une authorization par Bearer Token, API Key, Token ou X Token.
Par la suite vous pouvez nous communiquer l'authentification.

## Traitement des Réponses

### Réussite

En cas de succès, l'API renvoie un statut HTTP 200 avec un corps de réponse vide.


## Exemple de requête cURL

```bash
curl -X POST https://api.client.fr/leads \
-H "Content-Type: application/json" \
-H "Authorization: Bearer VOTRE_CLE_API" \
-d '{
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
}'
```

## Support

Pour toute question ou assistance technique, veuillez contacter le support d'Ici Formation à l'adresse tech@iciformation.fr ou a.stoj@iciformation.fr

---
