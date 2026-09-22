# ACADEE — Prospects IA dans l’Aube

Code source de la version publiée le 22 septembre 2026.

## Contenu

- `dist/index.html` : interface complète du CRM, styles et logique JavaScript.
- `dist/prospects.json` : données initiales des prospects.
- `.openai/hosting.json` : configuration de publication du Site.

## Utilisation locale

Le projet est une application HTML statique. Pour éviter les restrictions du navigateur lors du chargement du fichier JSON, lance un serveur HTTP dans le dossier `ACADEE_CRM_Sources`.

Avec Python installé :

```bash
python -m http.server 8080
```

Ouvre ensuite `http://localhost:8080/dist/` dans le navigateur.

## Données et intelligence artificielle

- Les données du CRM sont enregistrées dans le stockage local du navigateur.
- La recherche d’entreprises utilise l’API publique de l’Annuaire des Entreprises.
- La qualification actuelle est déterministe et fondée sur les paramètres ACADEE, le secteur, l’effectif et la zone géographique.
- Aucun modèle OpenAI n’est appelé dans cette version tant que l’intégration OpenAI Developers et une clé API serveur ne sont pas configurées.

## Confidentialité

Ne place jamais une clé API OpenAI directement dans `index.html`. Une intégration OpenAI doit passer par une fonction serveur avec une variable secrète.
