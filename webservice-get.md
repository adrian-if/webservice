# Documentation API GET - Ici Formation V1
Date de création : 26/06/2025

Date de dernière modification : 26/06/2025

## 📘 Vue d'ensemble

L'API *Ici Formation* permet de récupérer automatiquement les leads générés sur iciformation.fr. Cette documentation vous guide dans l'intégration du point d'accès permettant de **lister les mises en relation** effectuées via notre plateforme.

## ⚙️ Fonctionnement

1. Un utilisateur remplit un formulaire sur iciformation.fr  
2. Le lead est traité par nos systèmes internes  
3. Vous pouvez consulter la liste des leads en appelant notre **API REST sécurisée**

## Étapes de mise en place
- Configurer votre endpoint
- Nous vous communiquons un token d'authentification
- Effectuer un test avec notre équipe
- Vérifier la réception des données

## 🔌 Options d'intégration

### Pour les développeurs

- Intégration directe via **API REST** en `GET` (cette documentation)
- Intégration directe via [**API REST** en `POST `](https://github.com/adrian-if/webservice/blob/main/default.md)  

### Pour les non-développeurs

- Intégration indirecte via des outils comme Zapier, CRM ou Hubspot (version POST uniquement – [voir cette documentation](https://github.com/adrian-if/webservice/blob/main/hubspot.md))

---

## 🛠 Endpoint disponible

### `GET https://www.iciformation.fr/api/webservice/leads`

Permet de récupérer la liste des leads (mises en relation) sur une période donnée.
Par défaut nous envoyons les mises en relation des 3 derniers mois.

#### Paramètres

| Paramètre   | Type     | Obligatoire | Description                                                  |
|-------------|----------|-------------|--------------------------------------------------------------|
| `dateStart` | string   | Non         | Date de début au format `YYYY-MM-DD`. Défaut : -3 mois       |
| `dateEnd`   | string   | Non         | Date de fin au format `YYYY-MM-DD`. Défaut : aujourd'hui     |

---

## 📥 Authentification
 
Le token est à transmettre via l’en-tête suivant :

Authorization: Bearer <votre_token>

## Support

Pour toute question ou assistance technique, veuillez contacter le support d'Ici Formation à l'adresse tech@iciformation.fr ou a.stoj@iciformation.fr

---
