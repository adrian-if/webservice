
# Documentation API - Ici Formation V2
Date de création : 10/04/2024

## Introduction

L'API Ici Formation est conçue pour permettre aux clients de recevoir les leads de manière automatisée et en temps réel. Cette documentation vise à expliquer comment intégrer et utiliser l'API POST pour transmettre des leads.
Cette documentation est à destination de l'équipe technique du client souhaitant réceptionner les leads.

Si vous n'avez pas la possibilité de créer une url de réception pour réceptionner les leads vous pouvez utiliser un service tiers comme Zapier ou si vous utilisez le CRM Hubspot consultez la documentation correspondante. 

## Méthode HTTP

La méthode utilisée pour transmettre les données est POST.

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

## Traitement des Réponses

### Réussite

En cas de succès, l'API renvoie un statut HTTP 200 avec un corps de réponse vide.

### Erreurs

L'API peut renvoyer divers codes d'erreur, y compris :

- `400 Bad Request` : Le corps de la requête est mal formé ou incomplet.
- `401 Unauthorized` : La clé API est manquante ou invalide.
- `500 Internal Server Error` : Une erreur côté serveur a empêché le traitement de la requête.

Pour chaque erreur, un message explicatif est fourni pour aider à diagnostiquer le problème.

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
