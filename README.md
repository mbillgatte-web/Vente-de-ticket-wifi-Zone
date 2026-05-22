# WiFi Zone

Site statique de vente de tickets WiFi avec point d'entrée unique.

## Description

Ce projet contient plusieurs pages HTML représentant une application de vente de tickets WiFi. Une page `index.html` a été ajoutée comme point d'entrée unique et utilise un routage par hash pour charger dynamiquement les autres pages dans un conteneur principal.

## Pages

- `index.html` - point d'entrée unique et routeur
- `01-homepage-shop.html` - page d'accueil / boutique
- `02-checkout.html` - page de checkout et collecte d'informations
- `03-payment.html` - page de choix de paiement
- `04-confirmation.html` - page de confirmation de commande
- `05-payment-error.html` - page d'erreur de paiement
- `06-history.html` - page d'historique utilisateur
- `07-admin-dashboard.html` - tableau de bord admin
- `08-admin-tickets.html` - gestion des tickets admin

## Fonctionnalités principales

- Entrée unique via `index.html`
- Navigation interne gérée par les routes hash (`#home`, `#checkout`, `#payment`, `#confirmation`, `#history`, `#admin-dashboard`, etc.)
- Chargement des fichiers HTML existants dans le conteneur principal
- Simulations de navigation via `location.hash` pour les pages de paiement et confirmation
- Utilisation de `localStorage` pour stocker temporairement certaines données de navigation

## Instructions de lancement

1. Ouvrez un terminal dans le dossier du projet.
2. Démarrez un serveur HTTP local (recommandé, `file://` ne fonctionne pas toujours avec `fetch`).

### Avec Python 3

```bash
python -m http.server 8000
```

### Avec Node.js

```bash
npx http-server -p 8000
```

3. Ouvrez dans votre navigateur :

```text
http://localhost:8000/
```

4. Naviguez entre les pages via l'en-tête ou les boutons internes.

## Notes

- Les pages originales restent présentes et peuvent être modifiées indépendamment.
- `index.html` applique l'en-tête global, le footer et gère le chargement dynamique des vues.
- Pour des liens internes supplémentaires, adaptez les `href` vers les routes hash appropriées.
